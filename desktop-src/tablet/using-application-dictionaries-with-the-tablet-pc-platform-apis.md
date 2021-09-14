---
description: Para usar un diccionario de aplicaciones con Tablet PC API, primero debe crear un archivo con la lista de palabras para el diccionario de aplicaciones.
ms.assetid: 6abadad1-262b-4536-8846-1c06226dc18a
title: Uso de diccionarios de aplicaciones con las API de la plataforma de Tablet PC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fc0e444ad2213d945c0210d07c72f9540ae16be
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127267596"
---
# <a name="using-application-dictionaries-with-the-tablet-pc-platform-apis"></a>Uso de diccionarios de aplicaciones con las API de la plataforma de Tablet PC

Para usar un diccionario de aplicaciones con Tablet PC API, primero debe crear un archivo con la lista de palabras para el diccionario de aplicaciones.

La solución más fácil para esto es usar un archivo de texto que contenga una lista de las palabras. Cuando se carga la aplicación, lee el archivo de texto y crea un objeto [**WordList**](inkwordlist-class.md) a partir de la lista de palabras del archivo. Para cada [**RecognizerContext**](inkrecognizercontext-class.md) asociado al diccionario de aplicaciones, establezca la propiedad [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) del objeto **RecognizerContext** en la lista de palabras del archivo de texto.

En el ejemplo siguiente se muestra cómo crear un [**objeto WordList**](inkwordlist-class.md) a partir de una [colección StringCollection.](/dotnet/api/system.collections.specialized.stringcollection?view=netcore-3.1) En este ejemplo se supone que ya ha cargado la lista de palabras del disco y ha creado una colección StringCollection a partir de estas palabras.


```C++
using System.Collections.Specialized;
using Microsoft.Ink;
//...
RecognizerContext theRecognizerContext;
StringCollection theUserDictionary;
//... 
// Initialize theRecognizerContext and theUserDictionary objects here.
//...
WordList theUserWordList = new WordList();
foreach (string s in theUserDictionary)
{
    theUserWordList.Add(s);
}
theRecognizerContext.WordList = theUserWordList;
```



> [!Note]  
> La [**propiedad Strokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes) del [**objeto RecognizerContext**](inkrecognizercontext-class.md) debe estar vacía antes de establecer la [**propiedad WordList.**](inkwordlist-class.md) Si la [**propiedad Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) no está vacía, se produce una excepción. Además, las palabras nunca se deben agregar a una lista de palabras después de que se haya asignado a un **objeto RecognizerContext.** Las palabras que se agregan a la lista de palabras después de asignarse al objeto **RecognizerContext** no se actualizan en el reconocedor. Para actualizar la lista de palabras, debe reasignar el **objeto WordList** a la [**propiedad WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) del **objeto RecognizerContext.**

 

Para obtener la máxima precisión de reconocimiento, combine factoids con el diccionario de la aplicación en una relación ventajosa. Para obtener más información sobre la relación entre factoids y diccionarios de aplicaciones, vea [Understanding Word Lists, Recognizer Context y Factoids](understanding-wordlists--the-recognizercontext--and-factoids.md).

Para obtener un ejemplo del uso de diccionarios de aplicaciones con el control [InkEdit,](inkedit-control-reference.md) vea Uso de [un diccionario de aplicaciones con InkEdit.](using-an-application-dictionary-with-inkedit.md)

 

 
