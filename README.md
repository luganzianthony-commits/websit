<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Salon Home Delivery Service - Booking Form</title>
    <script src="https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4"></script>
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Plus Jakarta Sans', sans-serif;
            background-color: #f7e1c2;
        }
        /* Custom color classes matching the palette */
        .bg-cream { background-color: #f7e1c2; }
        .bg-warm-tan { background-color: #c68a57; }
        .bg-chocolate { background-color: #5c3823; }
        .bg-espresso { background-color: #361f12; }
        
        .text-cream { color: #f7e1c2; }
        .text-warm-tan { color: #c68a57; }
        .text-chocolate { color: #5c3823; }
        .text-espresso { color: #361f12; }

        .border-warm-tan { border-color: #c68a57; }
        .border-chocolate { border-color: #5c3823; }
        
        input:focus, select:focus, textarea:focus {
            outline: none;
            border-color: #5c3823;
            box-shadow: 0 0 0 2px rgba(92, 56, 35, 0.2);
        }
    </style>
</head>
<body class="min-h-screen py-10 px-4 sm:px-6">

    <div class="max-w-2xl mx-auto bg-white rounded-3xl shadow-2xl overflow-hidden border border-[#c68a57]/30">
        
        <!-- Header -->
        <div class="bg-[#361f12] text-white px-8 py-8 text-center relative overflow-hidden">
            <div class="absolute -right-10 -bottom-10 w-40 h-40 bg-[#c68a57]/20 rounded-full blur-2xl"></div>
            <span class="text-xs uppercase tracking-widest bg-[#c68a57] text-[#361f12] font-bold px-3 py-1 rounded-full inline-block mb-3">Mobile Salon Concierge</span>
            <h1 class="text-3xl font-bold tracking-tight mb-2">Home Delivery Service</h1>
            <p class="text-[#f7e1c2]/80 text-sm">Professional salon grooming & styling delivered right to your doorstep.</p>
        </div>

        <!-- Form Body -->
        <form id="salonBookingForm" class="p-6 sm:p-8 space-y-8">
            
            <!-- Section 1: Client Details -->
            <div>
                <h2 class="text-lg font-bold text-[#361f12] mb-4 flex items-center gap-2">
                    <span class="w-7 h-7 rounded-full bg-[#f7e1c2] text-[#5c3823] flex items-center justify-center text-sm font-bold">1</span>
                    Your Information
                </h2>
                <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                    <div>
                        <label class="block text-xs font-bold text-[#5c3823] uppercase mb-1">Full Name</label>
                        <input type="text" id="clientName" required placeholder="e.g. Nakato Sandra" class="w-full px-4 py-3 rounded-xl border border-[#c68a57]/40 bg-stone-50 text-stone-800 text-sm font-medium">
                    </div>
                    <div>
                        <label class="block text-xs font-bold text-[#5c3823] uppercase mb-1">Phone Number</label>
                        <input type="tel" id="clientPhone" required placeholder="e.g. +256 700 000000" class="w-full px-4 py-3 rounded-xl border border-[#c68a57]/40 bg-stone-50 text-stone-800 text-sm font-medium">
                    </div>
                </div>
                <div class="mt-4">
                    <label class="block text-xs font-bold text-[#5c3823] uppercase mb-1">Delivery Address & Area</label>
                    <input type="text" id="clientAddress" required placeholder="e.g. Kololo, Acacia Avenue, Plot 12" class="w-full px-4 py-3 rounded-xl border border-[#c68a57]/40 bg-stone-50 text-stone-800 text-sm font-medium">
                </div>
            </div>

            <!-- Section 2: Service Selection -->
            <div>
                <h2 class="text-lg font-bold text-[#361f12] mb-4 flex items-center gap-2">
                    <span class="w-7 h-7 rounded-full bg-[#f7e1c2] text-[#5c3823] flex items-center justify-center text-sm font-bold">2</span>
                    Select Services (UGX)
                </h2>
                
                <div class="space-y-3">
                    <!-- Service Item -->
                    <label class="flex items-center justify-between p-4 rounded-xl border border-[#c68a57]/30 bg-stone-50 hover:bg-[#f7e1c2]/30 cursor-pointer transition-all">
                        <div class="flex items-center gap-3">
                            <input type="checkbox" name="service" value="Executive Haircut & Styling" data-price="45000" class="w-5 h-5 accent-[#5c3823] rounded">
                            <div>
                                <p class="font-bold text-[#361f12] text-sm">Executive Haircut & Styling</p>
                                <p class="text-xs text-[#c68a57]">Precision cut, wash & blowdry</p>
                            </div>
                        </div>
                        <span class="font-bold text-[#5c3823] text-sm">45,000 UGX</span>
                    </label>

                    <!-- Service Item -->
                    <label class="flex items-center justify-between p-4 rounded-xl border border-[#c68a57]/30 bg-stone-50 hover:bg-[#f7e1c2]/30 cursor-pointer transition-all">
                        <div class="flex items-center gap-3">
                            <input type="checkbox" name="service" value="Professional Blowout & Silk Press" data-price="60000" class="w-5 h-5 accent-[#5c3823] rounded">
                            <div>
                                <p class="font-bold text-[#361f12] text-sm">Professional Blowout & Silk Press</p>
                                <p class="text-xs text-[#c68a57]">Smooth, shiny finish</p>
                            </div>
                        </div>
                        <span class="font-bold text-[#5c3823] text-sm">60,000 UGX</span>
                    </label>

                    <!-- Service Item -->
                    <label class="flex items-center justify-between p-4 rounded-xl border border-[#c68a57]/30 bg-stone-50 hover:bg-[#f7e1c2]/30 cursor-pointer transition-all">
                        <div class="flex items-center gap-3">
                            <input type="checkbox" name="service" value="Luxury Mani & Pedi Combo" data-price="70000" class="w-5 h-5 accent-[#5c3823] rounded">
                            <div>
                                <p class="font-bold text-[#361f12] text-sm">Luxury Mani & Pedi Combo</p>
                                <p class="text-xs text-[#c68a57]">Includes scrub & gel polish</p>
                            </div>
                        </div>
                        <span class="font-bold text-[#5c3823] text-sm">70,000 UGX</span>
                    </label>

                    <!-- Service Item -->
                    <label class="flex items-center justify-between p-4 rounded-xl border border-[#c68a57]/30 bg-stone-50 hover:bg-[#f7e1c2]/30 cursor-pointer transition-all">
                        <div class="flex items-center gap-3">
                            <input type="checkbox" name="service" value="Bridal / Event Makeup" data-price="120000" class="w-5 h-5 accent-[#5c3823] rounded">
                            <div>
                                <p class="font-bold text-[#361f12] text-sm">Bridal / Event Makeup</p>
                                <p class="text-xs text-[#c68a57]">Long-lasting glamorous finish</p>
                            </div>
                        </div>
                        <span class="font-bold text-[#5c3823] text-sm">120,000 UGX</span>
                    </label>

                    <!-- Service Item -->
                    <label class="flex items-center justify-between p-4 rounded-xl border border-[#c68a57]/30 bg-stone-50 hover:bg-[#f7e1c2]/30 cursor-pointer transition-all">
                        <div class="flex items-center gap-3">
                            <input type="checkbox" name="service" value="Hair Braiding / Cornrows" data-price="90000" class="w-5 h-5 accent-[#5c3823] rounded">
                            <div>
                                <p class="font-bold text-[#361f12] text-sm">Hair Braiding / Cornrows</p>
                                <p class="text-xs text-[#c68a57]">Neat professional styling</p>
                            </div>
                        </div>
                        <span class="font-bold text-[#5c3823] text-sm">90,000 UGX</span>
                    </label>
                </div>
            </div>

            <!-- Section 3: Date & Time -->
            <div>
                <h2 class="text-lg font-bold text-[#361f12] mb-4 flex items-center gap-2">
                    <span class="w-7 h-7 rounded-full bg-[#f7e1c2] text-[#5c3823] flex items-center justify-center text-sm font-bold">3</span>
                    Schedule Appointment
                </h2>
                <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                    <div>
                        <label class="block text-xs font-bold text-[#5c3823] uppercase mb-1">Preferred Date</label>
                        <input type="date" id="serviceDate" required class="w-full px-4 py-3 rounded-xl border border-[#c68a57]/40 bg-stone-50 text-stone-800 text-sm font-medium">
                    </div>
                    <div>
                        <label class="block text-xs font-bold text-[#5c3823] uppercase mb-1">Time Slot</label>
                        <select id="serviceTime" required class="w-full px-4 py-3 rounded-xl border border-[#c68a57]/40 bg-stone-50 text-stone-800 text-sm font-medium">
                            <option value="">Select time slot</option>
                            <option value="Morning (09:00 AM - 12:00 PM)">Morning (09:00 AM - 12:00 PM)</option>
                            <option value="Afternoon (12:00 PM - 03:00 PM)">Afternoon (12:00 PM - 03:00 PM)</option>
                            <option value="Late Afternoon (03:00 PM - 06:00 PM)">Late Afternoon (03:00 PM - 06:00 PM)</option>
                        </select>
                    </div>
                </div>
            </div>

            <!-- Summary & Submit -->
            <div class="bg-[#f7e1c2]/50 p-5 rounded-2xl border border-[#c68a57]/30 flex flex-col sm:flex-row items-center justify-between gap-4">
                <div>
                    <p class="text-xs font-bold uppercase text-[#5c3823]">Estimated Total</p>
                    <p id="totalPrice" class="text-2xl font-black text-[#361f12]">0 UGX</p>
                </div>
                <button type="submit" class="w-full sm:w-auto px-8 py-4 bg-[#361f12] hover:bg-[#5c3823] text-white font-bold rounded-xl shadow-lg transition-all text-sm tracking-wide">
                    Confirm Home Delivery Booking
                </button>
            </div>

        </form>
    </div>

    <!-- Success Modal -->
    <div id="successModal" class="fixed inset-0 bg-[#361f12]/80 backdrop-blur-sm hidden items-center justify-center p-4 z-50">
        <div class="bg-white rounded-3xl max-w-md w-full p-8 text-center space-y-4 shadow-2xl border border-[#c68a57]">
            <div class="w-16 h-16 bg-[#f7e1c2] text-[#5c3823] rounded-full flex items-center justify-center mx-auto text-3xl font-bold">✓</div>
            <h3 class="text-2xl font-bold text-[#361f12]">Booking Received!</h3>
            <p class="text-stone-600 text-sm">Thank you! Our mobile salon concierge will contact you shortly via phone call or WhatsApp to confirm your appointment details.</p>
            <button onclick="closeModal()" class="w-full py-3 bg-[#361f12] text-white font-bold rounded-xl text-sm hover:bg-[#5c3823] transition-all">
                Close & Done
            </button>
        </div>
    </div>

    <script>
        const checkboxes = document.querySelectorAll('input[name="service"]');
        const totalPriceEl = document.getElementById('totalPrice');
        const form = document.getElementById('salonBookingForm');
        const modal = document.getElementById('successModal');

        function calculateTotal() {
            let total = 0;
            checkboxes.forEach(cb => {
                if (cb.checked) {
                    total += parseInt(cb.dataset.price);
                }
            });
            totalPriceEl.textContent = total.toLocaleString() + ' UGX';
        }

        checkboxes.forEach(cb => {
            cb.addEventListener('change', calculateTotal);
        });

        form.addEventListener('submit', (e) => {
            e.preventDefault();
            const checkedCount = Array.from(checkboxes).filter(cb => cb.checked).length;
            if (checkedCount === 0) {
                alert('Please select at least one service.');
                return;
            }
            modal.classList.remove('hidden');
            modal.classList.add('flex');
        });

        function closeModal() {
            modal.classList.remove('flex');
            modal.classList.add('hidden');
            form.reset();
            calculateTotal();
        }
    </script>
</body>
</html>
