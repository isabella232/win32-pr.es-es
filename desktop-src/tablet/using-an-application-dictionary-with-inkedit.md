---
description: Para crear un diccionario de aplicaciones, es necesario establecer la propiedad WordList del objeto RecognizerContext.
ms.assetid: 24dbf617-fa16-44f1-ba59-d4d99b8f1375
title: Uso de un diccionario de aplicaciones con InkEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35b090b0822afba691012ef19d51068a18c3cf8d6c9afb9070f43f63cd86ef34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966644"
---
# <a name="using-an-application-dictionary-with-inkedit"></a>Uso de un diccionario de aplicaciones con InkEdit

Para crear un diccionario de aplicaciones, es necesario establecer la [**propiedad WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) del [**objeto RecognizerContext.**](inkrecognizercontext-class.md) El control [InkEdit](inkedit-control-reference.md) no expone el objeto **RecognizerContext,** por lo que no es posible establecer directamente la propiedad **WordList** del objeto **RecognizerContext** del control InkEdit.

Para usar un diccionario de aplicaciones con un control [InkEdit,](inkedit-control-reference.md) debe quitar los trazos del control InkEdit, pasarlos a un nuevo objeto [**RecognizerContext**](inkrecognizercontext-class.md) con la propiedad [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) establecida en un [**wordList**](inkwordlist-class.md) que contiene el diccionario de aplicaciones, almacenar los resultados de este objeto **RecognizerContext** y, a continuación, devolver los resultados al control InkEdit.

## <a name="example"></a>Ejemplo

En el código C \# siguiente se muestra un ejemplo de esta técnica.


```C++
private RecognizerContext rc;
private WordList wl;
private int wlSelStart;
private int wlSelLen;
private bool isRecoPending = false;

private void Form1_Load(object sender, EventArgs e)
{
  //event handlers must be attached for dictionary to work.
  inkEdit1.Recognition += new Microsoft.Ink.InkEditRecognitionEventHandler(inkEdit1_Recognition);
  inkEdit1.TextChanged += new EventHandler(inkEdit1_TextChanged);

  //create a WordList that contains the application dictionary
  wl = new WordList();
  //...
  //Add dictionary terms to the WordList
  //...

  // create a RecognizerContext for the WordList
  rc = inkEdit1.Recognizer.CreateRecognizerContext();
  rc.Factoid = Factoid.WordList;

  //set the RecognizerContext WordList to the newly created WordList
  rc.WordList = wl;

  //create a delegate for the new RecognizerContext
  rc.RecognitionWithAlternates += new

  RecognizerContextRecognitionWithAlternatesEventHandler(rc_Recognition);
}

void inkEdit1_TextChanged(object sender, EventArgs e)
{
  if (isRecoPending)
  {
    isRecoPending = false;
    rc.BackgroundRecognizeWithAlternates();
  }
}

private void inkEdit1_Recognition(object sender,
Microsoft.Ink.InkEditRecognitionEventArgs e)
{
  //store the start of the selection in wlSelStart
  wlSelStart = inkEdit1.SelectionStart;

  //store the length of the selection in wlSelLen
  wlSelLen = e.RecognitionResult.TopString.Length;

  //copy the strokes from the InkEdit control into the new
  // RecognizerContext
  rc.Strokes = e.RecognitionResult.Strokes.Ink.Clone().Strokes;
  isRecoPending = true;
}

private void rc_Recognition(object sender,
Microsoft.Ink.RecognizerContextRecognitionWithAlternatesEventArgs e)
{
  if (inkEdit1.InvokeRequired)
  {
    inkEdit1.Invoke(new RecognizerContextRecognitionWithAlternatesEventHandler(rc_Recognition),
      new object[] { sender, e });
    return;
  }

  //set the insertion point in the InkEdit control
  inkEdit1.SelectionStart = wlSelStart;
  inkEdit1.SelectionLength = wlSelLen;
  //insert the result from the new RecognizerContext 
  //into the InkEdit control
  inkEdit1.SelectedText = e.Result.TopString;
  inkEdit1.SelectionStart = inkEdit1.SelectionStart +
  e.Result.TopString.Length;
}

// Event handler for the form's closed event
private void Form1_Closed(object sender, System.EventArgs e)
{
  inkEdit1.Dispose();
  inkEdit1 = null;
  rc.Dispose();
  rc = null;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[InkEdit Control](/previous-versions/ms552265(v=vs.100))
</dt> <dt>

[Clase Microsoft.Ink.RecognizerContext](/previous-versions/ms552546(v=vs.100))
</dt> <dt>

[Clase Microsoft.Ink.Wordlist](/previous-versions/ms827589(v=msdn.10))
</dt> </dl>

 

 
