# ADR-form-fill-task2                                                                                                                
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Suspected Adverse Drug Reaction Reporting Form</title>
  <style>
    body { font-family: Arial, sans-serif; margin: 20px; line-height: 1.6; }
    h2, h3 { color: #2c3e50; }
    fieldset { border: 1px solid #ccc; margin-bottom: 15px; padding: 15px; }
    legend { font-weight: bold; padding: 0 5px; }
    .form-group { margin-bottom: 10px; }
    label { font-weight: bold; }
    input[type="text"], input[type="date"], textarea, select {
      width: 100%; padding: 6px; margin-top: 4px; box-sizing: border-box;
    }
    .inline-group { display: flex; gap: 15px; }
    .inline-group div { flex: 1; }
  </style>
</head>
<body>

  <h2>Suspected Adverse Drug Reaction (ADR) Reporting Form</h2>

  <form action="#" method="post">
    
    <!-- Section 1: Patient Information -->
    <fieldset>
      <legend>A. Patient Information</legend>
      <div class="inline-group">
        <div>
          <label for="initials">Patient Initials:</label>
          <input type="text" id="initials" name="initials" placeholder="e.g., RP" required>
        </div>
        <div>
          <label for="age">Age:</label>
          <input type="text" id="age" name="age" placeholder="e.g., 32 years">
        </div>
        <div>
          <label>Gender:</label><br>
          <input type="radio" id="male" name="gender" value="Male"> <label for="male">Male</label>
          <input type="radio" id="female" name="gender" value="Female"> <label for="female">Female</label>
        </div>
        <div>
          <label for="weight">Weight (kg):</label>
          <input type="text" id="weight" name="weight" placeholder="e.g., 65 kg">
        </div>
      </div>
    </fieldset>

    <!-- Section 2: Adverse Reaction Details -->
    <fieldset>
      <legend>B. Suspected Adverse Reaction</legend>
      <div class="inline-group">
        <div>
          <label for="reaction_start">Date Reaction Started:</label>
          <input type="date" id="reaction_start" name="reaction_start">
        </div>
        <div>
          <label for="reaction_stopped">Date of Recovery:</label>
          <input type="date" id="reaction_stopped" name="reaction_stopped">
        </div>
      </div>
      <div class="form-group" style="margin-top: 10px;">
        <label for="description">Description of Reaction / Problem:</label>
        <textarea id="description" name="description" rows="3" placeholder="Describe symptoms..."></textarea>
      </div>
    </fieldset>

    <!-- Section 3: Suspected Medication -->
    <fieldset>
      <legend>C. Suspected Medication(s)</legend>
      <div class="form-group">
        <label for="drug_name">Name (Brand/Generic):</label>
        <input type="text" id="drug_name" name="drug_name" placeholder="e.g., Amoxicillin">
      </div>
      <div class="inline-group">
        <div>
          <label for="dose">Dose:</label>
          <input type="text" id="dose" name="dose" placeholder="e.g., 500 mg">
        </div>
        <div>
          <label for="route">Route:</label>
          <input type="text" id="route" name="route" placeholder="e.g., Oral">
        </div>
        <div>
          <label for="frequency">Frequency:</label>
          <input type="text" id="frequency" name="frequency" placeholder="e.g., TID">
        </div>
      </div>
      <div class="inline-group" style="margin-top: 10px;">
        <div>
          <label for="date_started">Date Started:</label>
          <input type="date" id="date_started" name="date_started">
        </div>
        <div>
          <label for="date_stopped">Date Stopped:</label>
          <input type="date" id="date_stopped" name="date_stopped">
        </div>
      </div>
      <div class="form-group" style="margin-top: 10px;">
        <label for="indication">Indication / Prescribed For:</label>
        <input type="text" id="indication" name="indication" placeholder="e.g., Acute Bacterial Sinusitis">
      </div>
    </fieldset>

    <!-- Section 4: Outcome & Reporter Details -->
    <fieldset>
      <legend>D. Outcome & Reporter Info</legend>
      <div class="form-group">
        <label for="outcome">Outcome of Reaction:</label>
        <select id="outcome" name="outcome">
          <option value="recovered">Recovered</option>
          <option value="recovering">Recovering</option>
          <option value="fatal">Fatal</option>
          <option value="unknown">Unknown</option>
        </select>
      </div>
      <div class="form-group">
        <label for="reporter">Reporter Name & Professional Address:</label>
        <input type="text" id="reporter" name="reporter">
      </div>
    </fieldset>

    <input type="submit" value="Submit ADR Form" style="padding: 10px 20px; font-size: 16px; cursor: pointer;">
  </form>

</body>
</html>
