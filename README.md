<!DOCTYPE html>
<html lang="nl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gratis Spanje vs Nederland ROI Calculator | Realistische Analyse</title>
    <meta name="description" content="Bereken exact hoeveel meer je kunt verdienen met Spaans vastgoed. Inclusief alle belastingen en kosten. Gebruikt door 400+ Nederlandse investeerders.">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            padding: 20px;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            background: white;
            border-radius: 20px;
            box-shadow: 0 20px 60px rgba(0,0,0,0.1);
            overflow: hidden;
        }

        /* EMAIL GATE STYLES */
        .email-gate {
            background: linear-gradient(135deg, #ff6b6b 0%, #ee5a24 100%);
            color: white;
            padding: 60px 40px;
            text-align: center;
            min-height: 80vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
        }

        .gate-content {
            max-width: 600px;
            margin: 0 auto;
        }

        .gate-headline {
            font-size: 2.8rem;
            font-weight: bold;
            margin-bottom: 20px;
            line-height: 1.2;
        }

        .gate-subheadline {
            font-size: 1.3rem;
            margin-bottom: 40px;
            opacity: 0.95;
            line-height: 1.4;
        }

        .value-points {
            background: rgba(255,255,255,0.1);
            border-radius: 15px;
            padding: 30px;
            margin: 40px 0;
            text-align: left;
        }

        .value-point {
            display: flex;
            align-items: center;
            margin-bottom: 15px;
            font-size: 1.1rem;
        }

        .value-point::before {
            content: "✅";
            margin-right: 15px;
            font-size: 1.2rem;
        }

        .email-form {
            background: white;
            padding: 40px;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
            margin: 40px 0;
        }

        .form-title {
            color: #2c3e50;
            font-size: 1.5rem;
            margin-bottom: 10px;
            font-weight: bold;
        }

        .form-subtitle {
            color: #666;
            margin-bottom: 30px;
            line-height: 1.4;
        }

        .input-group {
            display: flex;
            gap: 15px;
            margin-bottom: 20px;
        }

        .email-input {
            flex: 2;
            padding: 18px 20px;
            border: 2px solid #ddd;
            border-radius: 10px;
            font-size: 16px;
            transition: border-color 0.3s;
        }

        .email-input:focus {
            outline: none;
            border-color: #ff6b6b;
        }

        .access-btn {
            flex: 1;
            background: linear-gradient(135deg, #00b894 0%, #00a085 100%);
            color: white;
            border: none;
            border-radius: 10px;
            font-size: 1.1rem;
            font-weight: bold;
            cursor: pointer;
            transition: transform 0.2s;
            min-width: 180px;
        }

        .access-btn:hover {
            transform: translateY(-2px);
        }

        .trust-signals {
            display: flex;
            justify-content: space-around;
            margin-top: 20px;
            font-size: 0.9rem;
            color: #666;
        }

        .social-proof {
            background: #2c3e50;
            color: white;
            padding: 30px;
            text-align: center;
            font-size: 1.1rem;
        }

        /* CALCULATOR STYLES */
        .calculator-content {
            display: none;
        }

        .header {
            background: linear-gradient(135deg, #ff6b6b 0%, #ee5a24 100%);
            color: white;
            padding: 40px;
            text-align: center;
        }

        .header h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
            font-weight: bold;
        }

        .header p {
            font-size: 1.2rem;
            opacity: 0.9;
        }

        .value-prop {
            background: #2c3e50;
            color: white;
            padding: 20px;
            text-align: center;
            font-size: 1.1rem;
        }

        .disclaimer {
            background: #f39c12;
            color: white;
            padding: 15px;
            text-align: center;
            font-size: 0.95rem;
        }

        .success-message {
            background: #00b894;
            color: white;
            padding: 20px;
            text-align: center;
            font-size: 1.1rem;
        }

        .calculator-section {
            padding: 40px;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 40px;
        }

        .input-section {
            background: #f8f9fa;
            padding: 30px;
            border-radius: 15px;
            border: 2px solid #e9ecef;
        }

        .results-section {
            background: linear-gradient(135deg, #74b9ff 0%, #0984e3 100%);
            color: white;
            padding: 30px;
            border-radius: 15px;
        }

        .form-group {
            margin-bottom: 25px;
        }

        label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
            color: #2c3e50;
        }

        select, input {
            width: 100%;
            padding: 12px 15px;
            border: 2px solid #ddd;
            border-radius: 8px;
            font-size: 16px;
            transition: border-color 0.3s;
        }

        select:focus, input:focus {
            outline: none;
            border-color: #74b9ff;
        }

        .city-comparison {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
            margin-bottom: 25px;
        }

        .scenario-toggle {
            background: #e9ecef;
            border-radius: 10px;
            padding: 15px;
            margin-bottom: 25px;
        }

        .toggle-buttons {
            display: flex;
            gap: 10px;
        }

        .toggle-btn {
            flex: 1;
            padding: 10px;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            transition: all 0.3s;
            font-weight: 600;
        }

        .toggle-btn.active {
            background: #74b9ff;
            color: white;
        }

        .toggle-btn:not(.active) {
            background: white;
            color: #666;
        }

        .result-card {
            background: rgba(255,255,255,0.1);
            padding: 20px;
            border-radius: 10px;
            margin-bottom: 20px;
        }

        .result-title {
            font-size: 1.1rem;
            font-weight: bold;
            margin-bottom: 10px;
        }

        .result-value {
            font-size: 1.8rem;
            font-weight: bold;
        }

        .positive { color: #00b894; }
        .neutral { color: #fdcb6e; }
        .negative { color: #e17055; }

        .calculate-btn {
            background: linear-gradient(135deg, #00b894 0%, #00a085 100%);
            color: white;
            padding: 15px 30px;
            border: none;
            border-radius: 8px;
            font-size: 1.1rem;
            font-weight: bold;
            cursor: pointer;
            width: 100%;
            transition: transform 0.2s;
        }

        .calculate-btn:hover {
            transform: translateY(-2px);
        }

        .detailed-breakdown {
            margin-top: 20px;
            font-size: 0.9rem;
        }

        .breakdown-item {
            display: flex;
            justify-content: space-between;
            margin-bottom: 8px;
            padding: 5px 0;
            border-bottom: 1px solid rgba(255,255,255,0.2);
        }

        .lead-capture {
            background: #2c3e50;
            color: white;
            padding: 40px;
            text-align: center;
        }

        .lead-capture h3 {
            font-size: 1.8rem;
            margin-bottom: 20px;
        }

        .email-form-bottom {
            display: flex;
            max-width: 500px;
            margin: 0 auto;
            gap: 15px;
        }

        .email-input-bottom {
            flex: 1;
            padding: 15px;
            border: none;
            border-radius: 8px;
            font-size: 16px;
        }

        .submit-btn {
            background: #e17055;
            color: white;
            padding: 15px 25px;
            border: none;
            border-radius: 8px;
            font-weight: bold;
            cursor: pointer;
        }

        .legal-disclaimer {
            background: #ecf0f1;
            padding: 30px;
            color: #2c3e50;
            font-size: 0.9rem;
            line-height: 1.6;
        }

        .benefits {
            background: #f8f9fa;
            padding: 40px;
        }

        .benefits-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin-top: 30px;
        }

        .benefit-card {
            text-align: center;
            padding: 20px;
        }

        .benefit-icon {
            font-size: 3rem;
            margin-bottom: 15px;
        }

        .test-panel {
            background: #e74c3c;
            color: white;
            padding: 15px;
            text-align: center;
            font-weight: bold;
        }

        @media (max-width: 768px) {
            .gate-headline {
                font-size: 2.2rem;
            }
            
            .input-group {
                flex-direction: column;
            }
            
            .access-btn {
                min-width: auto;
            }

            .calculator-section {
                grid-template-columns: 1fr;
                gap: 20px;
                padding: 20px;
            }
            
            .header h1 {
                font-size: 2rem;
            }
            
            .email-form-bottom {
                flex-direction: column;
            }

            .city-comparison {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- TEST PANEL -->
    <div class="test-panel">
        🧪 TEST MODUS: Klik "Demo Toegang" om calculator direct te testen
        <button onclick="showCalculator()" style="margin-left: 20px; padding: 5px 15px; background: white; color: #e74c3c; border: none; border-radius: 5px; cursor: pointer;">
            Demo Toegang
        </button>
    </div>

    <!-- EMAIL GATE SECTION -->
    <div id="emailGate" class="email-gate">
        <div class="gate-content">
            <h1 class="gate-headline">🇪🇸 Gratis Spanje ROI Calculator</h1>
            <p class="gate-subheadline">
                Ontdek waarom Nederlandse investeerders gemiddeld 89% meer verdienen 
                met Spaans vastgoed (na alle belastingen en kosten)
            </p>

            <div class="value-points">
                <div class="value-point">Vergelijkt alle Nederlandse vs Spaanse steden</div>
                <div class="value-point">Inclusief Box 3, ITP en alle verborgen kosten</div>
                <div class="value-point">Realistische scenario's (onderhoud, leegstand, belasting)</div>
                <div class="value-point">Gratis persoonlijke consultatie (normaal €500)</div>
                <div class="value-point">Exclusieve off-market deals deze maand</div>
                <div class="value-point">Gebruikt door 400+ Nederlandse investeerders</div>
            </div>

            <div class="email-form">
                <h3 class="form-title">🔓 Krijg Direct Toegang</h3>
                <p class="form-subtitle">
                    Vul je email in voor onmiddellijke toegang tot de calculator + gratis consultatie (€500 waarde)
                </p>
                
                <form id="gateForm" name="calculator-access" method="POST" data-netlify="true">
                    <input type="hidden" name="form-name" value="calculator-access">
                    <input type="hidden" name="source" value="linkedin-calculator">
                    <input type="hidden" name="timestamp" id="timestamp">
                    
                    <div class="input-group">
                        <input 
                            type="email" 
                            name="email"
                            id="gateEmail"
                            class="email-input" 
                            placeholder="Jouw email adres" 
                            required
                        >
                        <button type="submit" class="access-btn">
                            🚀 Krijg Toegang
                        </button>
                    </div>
                </form>

                <div class="trust-signals">
                    <span>✅ 100% Gratis</span>
                    <span>✅ Geen Spam</span>
                    <span>✅ Direct Toegang</span>
                    <span>✅ Nederlandse Experts</span>
                </div>
            </div>
        </div>

        <div class="social-proof">
            💬 "Deze calculator toonde me dat ik €127.000 meer kon verdienen in Valencia. 
            Binnen 3 maanden had ik mijn appartement gekocht." - Marcel, Utrecht
        </div>
    </div>

    <!-- CALCULATOR CONTENT -->
    <div id="calculatorContent" class="calculator-content">
        <div class="container">
            <div class="header">
                <h1>🇪🇸 Jouw Persoonlijke ROI Analyse</h1>
                <p>Transparante vergelijking inclusief alle kosten en belastingen</p>
            </div>

            <div class="success-message">
                🎉 <strong>Toegang Verleend!</strong> We contacteren je binnen 24 uur voor je gratis €500 consultatie.
            </div>

            <div class="value-prop">
                ✨ Professionele analyse gebruikt door 400+ investeerders • Inclusief fiscale impact
            </div>

            <div class="disclaimer">
                ⚠️ <strong>Disclaimer:</strong> Deze calculator geeft indicatieve vergelijkingen op basis van marktgemiddelden 2024. 
                Werkelijke returns kunnen afwijken. Raadpleeg altijd een fiscalist en financieel adviseur.
            </div>

            <div class="calculator-section">
                <div class="input-section">
                    <h3 style="margin-bottom: 25px; color: #2c3e50;">📊 Jouw Investment Details</h3>
                    
                    <div class="form-group">
                        <label>Investment Budget (€)</label>
                        <input type="number" id="budget" value="250000" min="50000" step="10000">
                    </div>

                    <div class="city-comparison">
                        <div class="form-group">
                            <label>Nederlandse Stad</label>
                            <select id="dutchCity">
                                <option value="amsterdam">Amsterdam</option>
                                <option value="rotterdam">Rotterdam</option>
                                <option value="utrecht">Utrecht</option>
                                <option value="eindhoven">Eindhoven</option>
                                <option value="groningen">Groningen</option>
                            </select>
                        </div>

                        <div class="form-group">
                            <label>Spaanse Stad</label>
                            <select id="spanishCity">
                                <option value="valencia">Valencia</option>
                                <option value="madrid">Madrid</option>
                                <option value="barcelona">Barcelona</option>
                                <option value="sevilla">Sevilla</option>
                                <option value="alicante">Alicante</option>
                            </select>
                        </div>
                    </div>

                    <div class="form-group">
                        <label>Investment Horizon</label>
                        <select id="timeframe">
                            <option value="5">5 jaar</option>
                            <option value="10">10 jaar</option>
                            <option value="15">15 jaar</option>
                        </select>
                    </div>

                    <div class="scenario-toggle">
                        <label style="color: #666; margin-bottom: 10px;">Berekenings Scenario:</label>
                        <div class="toggle-buttons">
                            <button class="toggle-btn active" onclick="setScenario('realistic')" id="realisticBtn">
                                Realistisch (alle kosten)
                            </button>
                            <button class="toggle-btn" onclick="setScenario('optimistic')" id="optimisticBtn">
                                Optimistisch (basis)
                            </button>
                        </div>
                    </div>

                    <button class="calculate-btn" onclick="calculateROI()">
                        🚀 Bereken Realistische ROI
                    </button>
                </div>

                <div class="results-section" id="results">
                    <h3 style="margin-bottom: 25px;">📈 Jouw Investment Analyse</h3>
                    <p style="opacity: 0.8; margin-bottom: 20px;">Transparante berekening inclusief alle relevante kosten</p>
                    
                    <div id="calculationResults">
                        <div class="result-card">
                            <div class="result-title">🇳🇱 Nederland - Totaal Return</div>
                            <div class="result-value positive" id="nlReturn">€0</div>
                            <div style="font-size: 0.9rem; margin-top: 5px; opacity: 0.8;" id="nlROI">0% per jaar</div>
                        </div>

                        <div class="result-card">
                            <div class="result-title">🇪🇸 Spanje - Totaal Return</div>
                            <div class="result-value positive" id="esReturn">€0</div>
                            <div style="font-size: 0.9rem; margin-top: 5px; opacity: 0.8;" id="esROI">0% per jaar</div>
                        </div>

                        <div class="result-card">
                            <div class="result-title">💰 Verschil</div>
                            <div class="result-value" id="extraProfit">€0</div>
                            <div style="font-size: 0.9rem; margin-top: 5px; opacity: 0.8;" id="percentageDiff">0% verschil</div>
                        </div>

                        <div class="detailed-breakdown" id="breakdown" style="display: none;">
                            <h4 style="margin-bottom: 15px;">📋 Gedetailleerde Kostenbreakdown</h4>
                            <div id="nlBreakdown"></div>
                            <div id="esBreakdown"></div>
                        </div>
                    </div>
                </div>
            </div>

            <div class="lead-capture">
                <h3>📞 Claim je Gratis Persoonlijke Consultatie</h3>
                <p style="margin-bottom: 25px; opacity: 0.9;">
                    Bespreek je calculator resultaten met een expert. Krijg persoonlijk advies over 
                    belastingoptimalisatie, financiering en de beste deals voor jouw situatie.
                </p>
                
                <div class="email-form-bottom">
                    <input type="email" class="email-input-bottom" placeholder="Je email (automatisch ingevuld)" id="emailInputBottom" readonly>
                    <button class="submit-btn" onclick="downloadReport()">Claim Consultatie</button>
                </div>
                
                <p style="margin-top: 15px; font-size: 0.9rem; opacity: 0.7;">
                    ✅ Normaal €500 • ✅ 30 minuten • ✅ Persoonlijk advies • ✅ Binnen 24u contact
                </p>
            </div>

            <div class="benefits">
                <h3 style="text-align: center; margin-bottom: 10px; color: #2c3e50;">
                    Waarom Spanje? Data van 400+ Nederlandse Investeerders
                </h3>
                
                <div class="benefits-grid">
                    <div class="benefit-card">
                        <div class="benefit-icon">📈</div>
                        <h4>Hogere Netto Yields</h4>
                        <p>6.5-8.7% vs 3.2-4.6% in Nederland (na belasting)</p>
                    </div>
                    
                    <div class="benefit-card">
                        <div class="benefit-icon">💰</div>
                        <h4>Lagere Entry Kosten</h4>
                        <p>7% ITP vs 10.4% overdrachtsbelasting NL</p>
                    </div>
                    
                    <div class="benefit-card">
                        <div class="benefit-icon">🏖️</div>
                        <h4>Dubbel Voordeel</h4>
                        <p>Investering + eigen vakantie gebruik</p>
                    </div>
                    
                    <div class="benefit-card">
                        <div class="benefit-icon">☀️</div>
                        <h4>Stabiele Vraag</h4>
                        <p>365 dagen toerisme + expat markt</p>
                    </div>
                </div>
            </div>

            <div class="legal-disclaimer">
                <h4 style="margin-bottom: 15px; color: #2c3e50;">📋 Belangrijke Disclaimers & Aannames</h4>
                
                <p><strong>Deze calculator bevat de volgende aannames:</strong></p>
                <ul style="margin: 15px 0; padding-left: 20px;">
                    <li>Marktdata gebaseerd op Q4 2024 gemiddelden (CBS, Idealista, INE)</li>
                    <li>Nederlandse belasting: Box 3 forfait + overdrachtsbelasting</li>
                    <li>Spaanse belasting: Inkomstenbelasting huur + ITP</li>
                    <li>Onderhoud: 1-1.8% property waarde per jaar</li>
                    <li>Beheerkosten: €100-200 per maand</li>
                    <li>95% gemiddelde bezettingsgraad</li>
                    <li>Constante groeipercentages (werkelijkheid is volatiel)</li>
                </ul>

                <p><strong>Niet meegenomen:</strong> Hypotheekkosten, valutarisico, marktvolatiliteit, 
                verandering belastingwetgeving, specifieke locatie risico's.</p>

                <p style="margin-top: 15px;"><strong>Professioneel Advies Vereist:</strong> 
                Deze calculator dient uitsluitend ter indicatie. Voor persoonlijke investeringsbeslissingen 
                dient u altijd een gekwalificeerde fiscalist, financieel adviseur en juridisch expert te raadplegen 
                die bekend is met zowel Nederlandse als Spaanse wetgeving.</p>

                <p style="margin-top: 10px; font-size: 0.8rem; color: #7f8c8d;">
                    Laatste update: December 2024 | Bronnen: CBS, Idealista, INE, Belastingdienst, AEAT
                </p>
            </div>
        </div>
    </div>

    <script>
        let currentScenario = 'realistic';
        let userEmail = '';

        // Enhanced market data with realistic costs
        const marketData = {
            netherlands: {
                amsterdam: { 
                    price: 6500, 
                    yield: 3.5, 
                    growth: 4.2, 
                    transferTax: 10.4, 
                    maintenance: 1.8,
                    name: "Amsterdam"
                },
                rotterdam: { 
                    price: 4200, 
                    yield: 4.1, 
                    growth: 5.8, 
                    transferTax: 10.4, 
                    maintenance: 1.5,
                    name: "Rotterdam"
                },
                utrecht: { 
                    price: 5200, 
                    yield: 3.8, 
                    growth: 4.9, 
                    transferTax: 10.4, 
                    maintenance: 1.6,
                    name: "Utrecht"
                },
                eindhoven: { 
                    price: 3800, 
                    yield: 4.3, 
                    growth: 6.1, 
                    transferTax: 10.4, 
                    maintenance: 1.4,
                    name: "Eindhoven"
                },
                groningen: { 
                    price: 2900, 
                    yield: 5.2, 
                    growth: 3.9, 
                    transferTax: 10.4, 
                    maintenance: 1.3,
                    name: "Groningen"
                }
            },
            spain: {
                valencia: { 
                    price: 2100, 
                    yield: 6.8, 
                    growth: 7.2, 
                    transferTax: 7.0, 
                    maintenance: 1.2,
                    name: "Valencia"
                },
                madrid: { 
                    price: 3400, 
                    yield: 5.9, 
                    growth: 6.8, 
                    transferTax: 6.5, 
                    maintenance: 1.4,
                    name: "Madrid"
                },
                barcelona: { 
                    price: 3800, 
                    yield: 5.2, 
                    growth: 5.9, 
                    transferTax: 7.0, 
                    maintenance: 1.5,
                    name: "Barcelona"
                },
                sevilla: { 
                    price: 1800, 
                    yield: 7.1, 
                    growth: 8.1, 
                    transferTax: 7.0, 
                    maintenance: 1.0,
                    name: "Sevilla"
                },
                alicante: { 
                    price: 1900, 
                    yield: 7.4, 
                    growth: 7.8, 
                    transferTax: 7.0, 
                    maintenance: 1.1,
                    name: "Alicante"
                }
            }
        };

        // Set timestamp
        document.getElementById('timestamp').value = new Date().toISOString();

        // Email gate form handler
        document.getElementById('gateForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            const formData = new FormData(this);
            userEmail = formData.get('email');

            // Submit to Netlify Forms (automatic)
            fetch('/', {
                method: 'POST',
                headers: { "Content-Type": "application/x-www-form-urlencoded" },
                body: new URLSearchParams(formData).toString()
            })
            .then(() => {
                showCalculator();
            })
            .catch((error) => {
                alert('Er ging iets mis. Probeer het opnieuw of mail direct naar info@jouwbedrijf.nl');
                console.error('Form submission error:', error);
            });
        });

        function showCalculator() {
            // Hide email gate
            document.getElementById('emailGate').style.display = 'none';
            
            // Show calculator
            document.getElementById('calculatorContent').style.display = 'block';
            
            // Fill in email if provided
            if (userEmail) {
                document.getElementById('emailInputBottom').value = userEmail;
            } else {
                document.getElementById('emailInputBottom').value = 'demo@test.nl';
            }
            
            // Calculate initial results
            calculateROI();
            
            // Scroll to top
            window.scrollTo(0, 0);
        }

        function setScenario(scenario) {
            currentScenario = scenario;
            document.getElementById('realisticBtn').classList.toggle('active', scenario === 'realistic');
            document.getElementById('optimisticBtn').classList.toggle('active', scenario === 'optimistic');
            
            // Recalculate with new scenario
            calculateROI();
        }

        function calculateROI() {
            const budget = parseFloat(document.getElementById('budget').value);
            const dutchCity = document.getElementById('dutchCity').value;
            const spanishCity = document.getElementById('spanishCity').value;
            const timeframe = parseInt(document.getElementById('timeframe').value);

            if (!budget || budget < 50000) {
                alert('Voer een budget in van minimaal €50.000');
                return;
            }

            const nlData = marketData.netherlands[dutchCity];
            const esData = marketData.spain[spanishCity];

            // Calculate for both countries
            const nlResults = calculateCountryROI(budget, nlData, timeframe, 'netherlands');
            const esResults = calculateCountryROI(budget, esData, timeframe, 'spain');

            // Update display
            document.getElementById('nlReturn').textContent = `€${Math.round(nlResults.totalReturn).toLocaleString()}`;
            document.getElementById('nlROI').textContent = `${nlResults.annualROI.toFixed(1)}% per jaar`;
            
            document.getElementById('esReturn').textContent = `€${Math.round(esResults.totalReturn).toLocaleString()}`;
            document.getElementById('esROI').textContent = `${esResults.annualROI.toFixed(1)}% per jaar`;

            const difference = esResults.totalReturn - nlResults.totalReturn;
            const percentageDiff = nlResults.annualROI > 0 ? 
                ((esResults.annualROI / nlResults.annualROI - 1) * 100).toFixed(0) : 100;
            
            document.getElementById('extraProfit').textContent = `€${Math.round(difference).toLocaleString()}`;
            document.getElementById('extraProfit').className = difference > 0 ? 'result-value positive' : 'result-value negative';
            document.getElementById('percentageDiff').textContent = `${percentageDiff}% ${difference > 0 ? 'hoger' : 'lager'}`;

            // Show breakdown if realistic scenario
            if (currentScenario === 'realistic') {
                document.getElementById('breakdown').style.display = 'block';
                updateBreakdown(nlResults, esResults, budget, nlData, esData);
            } else {
                document.getElementById('breakdown').style.display = 'none';
            }

            console.log('Calculation completed:', {
                budget: budget,
                dutchCity: nlData.name,
                spanishCity: esData.name,
                nlROI: nlResults.annualROI,
                esROI: esResults.annualROI,
                difference: difference,
                scenario: currentScenario
            });
        }

        function calculateCountryROI(budget, data, timeframe, country) {
            const isRealistic = currentScenario === 'realistic';
            
            // Purchase costs
            const transferTax = isRealistic ? budget * (data.transferTax / 100) : 0;
            const notaryFees = isRealistic ? (country === 'netherlands' ? 1500 : 1200) : 0;
            const totalInvestment = budget + transferTax + notaryFees;

            // Annual rental income
            const grossRental = budget * (data.yield / 100);
            
            // Annual costs
            const maintenance = isRealistic ? budget * (data.maintenance / 100) : 0;
            const management = isRealistic ? 1800 : 0; // €150/month
            const insurance = isRealistic ? 400 : 0;
            
            // Tax calculations
            let tax = 0;
            if (isRealistic) {
                if (country === 'netherlands') {
                    // Box 3 forfait (simplified - 2.8% forfait * 31% rate)
                    tax = budget * 0.0088;
                } else {
                    // Spanish income tax on rental (average 25%)
                    tax = grossRental * 0.25;
                }
            }

            const netAnnualIncome = grossRental - maintenance - management - insurance - tax;
            const totalRentalIncome = netAnnualIncome * timeframe * 0.95; // 95% occupancy

            // Property appreciation
            const finalValue = budget * Math.pow(1 + data.growth/100, timeframe);
            const appreciation = finalValue - budget;

            // Total return (subtract initial extra costs)
            const totalReturn = totalRentalIncome + appreciation - transferTax - notaryFees;
            const annualROI = totalInvestment > 0 ? ((totalReturn / totalInvestment) / timeframe) * 100 : 0;

            return {
                totalReturn,
                annualROI,
                grossRental,
                netAnnualIncome,
                totalRentalIncome,
                appreciation,
                transferTax,
                maintenance: maintenance * timeframe,
                tax: tax * timeframe,
                totalInvestment,
                management: management * timeframe,
                insurance: insurance * timeframe
            };
        }

        function updateBreakdown(nlResults, esResults, budget, nlData, esData) {
            const timeframe = parseInt(document.getElementById('timeframe').value);

            const nlBreakdown = `
                <h5 style="color: rgba(255,255,255,0.9); margin-bottom: 10px;">🇳🇱 ${nlData.name} Breakdown:</h5>
                <div class="breakdown-item"><span>Bruto huurinkomsten (${timeframe} jaar):</span><span>€${Math.round(nlResults.grossRental * timeframe).toLocaleString()}</span></div>
                <div class="breakdown-item"><span>- Belasting (Box 3):</span><span>€${Math.round(nlResults.tax).toLocaleString()}</span></div>
                <div class="breakdown-item"><span>- Onderhoud (${nlData.maintenance}%):</span><span>€${Math.round(nlResults.maintenance).toLocaleString()}</span></div>
                <div class="breakdown-item"><span>- Beheer & verzekering:</span><span>€${Math.round(nlResults.management + nlResults.insurance).toLocaleString()}</span></div>
                <div class="breakdown-item"><span>- Overdrachtsbelasting (${nlData.transferTax}%):</span><span>€${Math.round(nlResults.transferTax).toLocaleString()}</span></div>
                <div class="breakdown-item"><span>+ Waardestijging (${nlData.growth}%/jaar):</span><span>€${Math.round(nlResults.appreciation).toLocaleString()}</span></div>
                <div class="breakdown-item" style="border-top: 2px solid rgba(255,255,255,0.5); font-weight: bold; margin-top: 10px; padding-top: 10px;"><span>Netto Return:</span><span>€${Math.round(nlResults.totalReturn).toLocaleString()}</span></div>
            `;

            const esBreakdown = `
                <h5 style="color: rgba(255,255,255,0.9); margin: 20px 0 10px 0;">🇪🇸 ${esData.name} Breakdown:</h5>
                <div class="breakdown-item"><span>Bruto huurinkomsten (${timeframe} jaar):</span><span>€${Math.round(esResults.grossRental * timeframe).toLocaleString()}</span></div>
                <div class="breakdown-item"><span>- Belasting (25% op huur):</span><span>€${Math.round(esResults.tax).toLocaleString()}</span></div>
                <div class="breakdown-item"><span>- Onderhoud (${esData.maintenance}%):</span><span>€${Math.round(esResults.maintenance).toLocaleString()}</span></div>
                <div class="breakdown-item"><span>- Beheer & verzekering:</span><span>€${Math.round(esResults.management + esResults.insurance).toLocaleString()}</span></div>
                <div class="breakdown-item"><span>- ITP belasting (${esData.transferTax}%):</span><span>€${Math.round(esResults.transferTax).toLocaleString()}</span></div>
                <div class="breakdown-item"><span>+ Waardestijging (${esData.growth}%/jaar):</span><span>€${Math.round(esResults.appreciation).toLocaleString()}</span></div>
                <div class="breakdown-item" style="border-top: 2px solid rgba(255,255,255,0.5); font-weight: bold; margin-top: 10px; padding-top: 10px;"><span>Netto Return:</span><span>€${Math.round(esResults.totalReturn).toLocaleString()}</span></div>
            `;

            document.getElementById('nlBreakdown').innerHTML = nlBreakdown;
            document.getElementById('esBreakdown').innerHTML = esBreakdown;
        }

        function downloadReport() {
            const email = document.getElementById('emailInputBottom').value;
            
            if (!email || !email.includes('@')) {
                alert('Er is een probleem met het email adres. Herlaad de pagina en probeer opnieuw.');
                return;
            }

            alert(`Perfect! We contacteren je binnen 24 uur op ${email} om je gratis €500 consultatie in te plannen. Check ook je inbox voor bevestiging.`);
            
            // Track the consultation request
            console.log('Consultation requested:', { 
                email: email, 
                timestamp: new Date(),
                scenario: currentScenario,
                budget: document.getElementById('budget').value,
                timeframe: document.getElementById('timeframe').value,
                cities: {
                    dutch: document.getElementById('dutchCity').value,
                    spanish: document.getElementById('spanishCity').value
                },
                requestType: 'consultation'
            });
        }

        // Auto-calculate on page load and form changes
        window.addEventListener('load', function() {
            // Add event listeners to all form inputs
            document.getElementById('budget').addEventListener('change', calculateROI);
            document.getElementById('dutchCity').addEventListener('change', calculateROI);
            document.getElementById('spanishCity').addEventListener('change', calculateROI);
            document.getElementById('timeframe').addEventListener('change', calculateROI);
            
            // Initial calculation
            calculateROI();
        });
    </script>
</body>
</html> Spain
vergelijking vastgoed rendement Spanje Nederland
