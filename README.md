# README
   
<div class="container-sm p-3 mb-3 bg-info text-white">
    <%= form_with(model: @article, local: true) do |f| %>
        <div class="row mb-3 justify-content-md-center">
                <label for="ArticleTitle" class="col-sm-2 col-form-label"><%= f.label :title %></label>
                <div class="col-6">
                    <input type="text" class="form-control" id="ArticleTitle" placeholder: f.text_field :title >
                </div>
        </div>
        <div class="mb-3 row justify-content-md-center">
            <label for="ArticleDescription" class="col-sm-2 col-form-label"><%= f.label :description %></label>
            <div class="col-6">
                <textarea class="form-control" id="ArticleDescription" rows="10" placeholder: f.text_area :description></textarea>
            </div>
        </div>
        <div class="text-center">
            <%= link_to 'Create Article', article_path(f), class: "btn btn-primary" %>
        </div>
    <% end %>
</div>