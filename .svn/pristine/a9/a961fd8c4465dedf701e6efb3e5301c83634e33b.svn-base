import moment from "moment"

let fetchTime = ()=>{
  return new Promise((resolve)=>{
    let time = moment().format('H:mm:ss')

    resolve(time)
  })
}

const winWidth = window.innerWidth || document.documentElement.clientWidth
                  || document.getElementsByTagName('body')[0].clientWidth

let Clock = ()=>{
  let rootNode = document.createElement("div")
  let newContent = document.createTextNode(moment().format('H:mm:ss'))
  rootNode.appendChild(newContent)
  Object.assign(rootNode.style, {
    marginTop: "100px",
    marginLeft: `${(winWidth-130) / 2.0}px`,
    fontSize: "30px",
    color: "green",
  })

  setInterval(()=>{
    fetchTime().then(time => {
      newContent.nodeValue = time
    })
  }, 1000)

  return rootNode
}

export default Clock
