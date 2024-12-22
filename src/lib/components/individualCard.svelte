<script>
	let members = [{ name: 'mama', photo: 'src/lib/assets/mama.jpeg' }];
	let winner = members[Math.floor(Math.random() * members.length)];
</script>

<div class="pokemonContainer">
	<div class="innerContainer">
		<div class="photoContainer">
			<img src={winner.photo} alt="winner" class="photo" />
		</div>

		<div class="contentExcludingImg">
			<h2>
				{winner.name}
			</h2>
			<div class="attackContainerIncludingHearts">
				<div class="heartContainer">
					<img src="src/lib/assets/heart.png" alt="" />
					<img src="src/lib/assets/heart.png" alt="" />
					<img src="src/lib/assets/heart.png" alt="" />
					<img src="src/lib/assets/heart.png" alt="" />
				</div>
				<div class="attackContainerExcludingHearts">
				<div class="attackTitle">
					<h2>Espresso Blitz</h2>
				</div>

				<div class="attackDescription">
					<p>
						This woman releases a frenzied barrage of coffee-fueled energy beams, leaving her
						opponents jittery and disoriented.
					</p>
				</div>
			</div>
			</div>

			<button>ATTACK!</button>
		</div>
	</div>
</div>

<style>
	.pokemonContainer {
		position: relative;
		width: 50%;
		height: auto;
		border: 1px solid rgb(216, 215, 215);
		border-radius: 2%;
		box-shadow: 0 10px 8px 0 rgba(0, 0, 0, 0.19);
		padding: 0;
		overflow: hidden;
		background-color: rgb(255, 241, 196);
	}

	.innerContainer {
		background-color: rgb(198, 178, 155);
		position: relative;
		margin: 20px;
	}
	.contentExcludingImg {
		position: relative;
		padding: 10px 20px;
	}
	.heartContainer {
		display: flex;
		width: 40%;			
		flex-wrap: wrap;
	}

	.heartContainer img {
		width: 50%;

	}

	.photoContainer {
		background-color: rgb(247, 246, 244);
	}

	.photo {
		display: block;
		margin: auto;
	}

	.attackContainerIncludingHearts {display: flex;}
	.attackContainerExcludingHearts{display: flex; flex-direction: column;}
	button {
		font-size: large;
		font-weight: bold;
		height: 40px;
		width: 100%;
		border: #fff;
		border-radius: 8px;
		background-color: rgb(61, 138, 246);
		color: #fff;
		transition: background-color 0.2s;
	}

	button:hover {
		background-color: rgb(17, 82, 174);
	}

	button:focus,
	button:active {
		background-color: rgb(16, 40, 77);
		transition: none;
	}
	button:disabled {
		background-color: rgb(176, 171, 171);
		transition: none;
	}

	@keyframes moveMaxHit {
		from {
			transform: translateY(0px);
			opacity: 1;
		}
		to {
			transform: translateY(-125px);
			opacity: 0;
		}
	}
</style>
