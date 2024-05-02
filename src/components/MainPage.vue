<template>
    <h1>{{ msg }}</h1>
    <h1>{{ infomus }}</h1>
    <div className="page">
  
            <div key={card.id}>
              <div className="card">
                <img
                  className="main_img"
                  src={card.snippet.thumbnails.medium.url}
                  alt="Card_IMG"
                />
                <div className="statistics">
                  <button className="commentes">
                    <SVGicons id="comments" />
                  </button>
                  <div className="views">{card.statistics.likeCount}</div>
                  <button className="commentes">
                    <SVGicons id="viewed" />
                  </button>
                  <div className="likes">{card.statistics.viewCount}</div>
                  <button className="commentes">
                    <SVGicons id="likes" />
                  </button>
                  <div className="dislikes">{card.statistics.dislikeCount}</div>
                  <button className="commentes">
                    <SVGicons id="dislike" />
                  </button>
                  <div className="comments">{card.statistics.commentCount}</div>
                </div>
                <div className="titile">{card.snippet.title}</div>
                <a>
                  <button
                    id="more"
                  >
                    more...
                  </button>
                </a>
              </div>
            </div>

          <!-- <Modal isOpen={!!modalData} onRequestClose={onClose}>
            {modalData && ( -->
              <div className="container">
                <a href="main">
                  <img src="../assets/back_button.png" alt="" />
                </a>
                <div className="main_flex">
                  <img src={modalData.snippet.thumbnails.medium.url} alt="" />
                  <div className="information">
                    <div className="text_info">
                      <div className="titltes">
                        <p className="title">{modalData.snippet.publishedAt}</p>
                        <p className="time">{modalData.id}</p>
                        <p className="time">{modalData.snippet.description}</p>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            <!-- )}
          </Modal> -->
        </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data(){
    return{
      infomus:'Музыкальный плеер',
    }
  }
  
}
</script>

<style scoped>
.hello{
  display: flex;
  flex-direction: row;
  justify-content: space-around;
}
</style>
