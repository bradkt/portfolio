Instructor Notes (https://www.udacity.com/course/viewer#!/c-ud304/l-2794148535/e-2730818615/m-2730818617)
			http://udacity.github.io/frontend-nanodegree-styleguide/

Be sure both the Bootstrap and JQuery JavaScript files are linked in the head element of your html file.

The Bootstrap JavaScript file is dependent on JQuery version 1.9 or higher. JQuery can be downloaded here: http://jquery.com/download

Once downloaded, place the JQuery file in the 'js' directory in the Bootstrap file structure.

Then link the JQuery and Bootstrap files to the head element in the HTML document in this order, replacing [JQuery file name] with the file name of the JQuery file you downloaded.:

<script type="text/javascript" src="js/[JQuery file name]"></script>
<script type="text/javascript" src="js/bootstrap.min.js"></script>
You will need several modals, one for each project for which you want to provide more information.

You have to change the id (as well as the title, image and description) for each modal to be unique. Then, you need to add a couple of data attributes to the element that will launch the modal. In this case, that element is the image of the portfolio project. You have to add the following attributes:

data-toggle="modal" data-target="#myModal"
For example, if you assigned id "project1" to the modal, the code for the first image would be:

<img class="img-responsive" src="images/555.jpeg" data-toggle="modal" data-target="#project1">
We slightly simplified the original Bootstrap examples that can be found here, but feel free to use any of the examples in the Bootstrap documentation.

Copy the following code and paste it in your html file, just above the closing </body> tag.

<!-- Modal -->
<div class="modal fade" id="project1" tabindex="-1" role="dialog" aria-labelledby="myModalLabel" aria-hidden="true">
  <div class="modal-dialog">
    <div class="modal-content">
      <div class="modal-header">
        <h4 class="modal-title" id="myModalLabel">Favorite App Page</h4>
      </div>
      <div class="modal-body">
        <img class="img-responsive" src="images/555.jpeg">
        This was my first project in this class. I learned a lot about HTML and CSS.
      </div>
      <div class="modal-footer">
        <button type="button" class="btn btn-default" data-dismiss="modal">Close</button>
      </div>
    </div>
  </div>
</div>