# 3-D
 A Bisection Reinforcement Learning Approach to 3-D Indoor Localization
 !
"Although the basic Q-learning method with networks of two to three layers in our current implementation already shows superior empirical performance, applying more advanced deep learning techniques may further improve the model (e.g., speed up or stabilize training, or improve accuracy)."

#"Şu anki uygulamamızda iki ila üç katmanlı ağlarla temel Q-öğrenme yöntemini kullandığımız halde, daha ileri düzey derin öğrenme tekniklerinin kullanılması modelin performansını daha da artırabilir (örneğin, eğitimi hızlandırabilir veya istikrarlı hale getirebilir veya doğruluğu artırabilir)."

"We have tested the proposed approach on three data sets in both single-floor and multifloor settings."

#"Önerilen yaklaşımı tek katlı ve çok katlı ayarlarda üç veri setinde test ettik."

"We hope that truly 3-D indoor data sets (continuous in the vertical direction) will be available in the near future, which may be the best scenario to demonstrate the advantages of this approach."

#"Yakın gelecekte, dikey yönde sürekli olan gerçek 3B iç mekan veri setlerinin mevcut olmasını umuyoruz. Bu, bu yaklaşımın avantajlarını en iyi şekilde göstermek için en iyi senaryo olabilir."

YAZILA KODUN AÇIKLAMALARI

GEREKLİ KÜTÜPHANAELER İMPORT EDİLİR.

 __init__(self, state_size, action_size, config=Config()): DQNAgent'in yapıcı metodu, modelin başlatılmasını, hiperparametrelerin ayarlanmasını ve bellek deque'sinin oluşturulmasını gerçekleştirir.

 _rest_epsilon_on_test(self): Test aşamasında keşif (exploration) oranını sıfırlamak için kullanılır.

_build_model(self): Derin Q-öğrenme modelini oluşturur. Model, ardışık (Sequential) bir yapıdadır ve tam bağlı (Dense) ve dropout katmanlarından oluşur.

_choose_action(self, state): Durum temsilini alarak bir aksiyon seçer. Epsilon değerine bağlı olarak rasgele bir aksiyon seçebilir veya Q değerlerine dayanarak en iyi aksiyonu seçebilir.

_store_transition(self, state, action, reward, next_state, done): Geçişleri hafızaya kaydeder. Her geçiş, bir durum, bir aksiyon, bir ödül, bir sonraki durum ve bir bitiş durumu içerir.

_learn(self, batch_size): Modeli öğrenmek için kullanılır. Rasgele bir örnekleme (minibatch) alarak, beklenen Q değerlerini hesaplar ve modeli eğitir.













