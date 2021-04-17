---
description: Para usar un diccionario de aplicación con la API de Tablet PC, primero debe crear un archivo con la lista de palabras del Diccionario de la aplicación.
ms.assetid: 6abadad1-262b-4536-8846-1c06226dc18a
title: Uso de diccionarios de aplicación con las API de la plataforma de Tablet PC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fc0e444ad2213d945c0210d07c72f9540ae16be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686750"
---
# <a name="using-application-dictionaries-with-the-tablet-pc-platform-apis"></a>Uso de diccionarios de aplicación con las API de la plataforma de Tablet PC

Para usar un diccionario de aplicación con la API de Tablet PC, primero debe crear un archivo con la lista de palabras del Diccionario de la aplicación.

La solución más sencilla es usar un archivo de texto que contenga una lista de las palabras. Cuando se carga la aplicación, lee el archivo de texto y crea [**un objeto**](inkwordlist-class.md) de lista de palabras a partir de la lista de palabras del archivo. Para cada [**RecognizerContext**](inkrecognizercontext-class.md) asociado al Diccionario de aplicación, establezca la propiedad lista de [**palabras**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) del objeto **RecognizerContext** en la lista de palabras del archivo de texto.

En el ejemplo siguiente se muestra cómo crear un objeto de una colección de [**palabras**](inkwordlist-class.md) a partir de una colección [StringCollection](/dotnet/api/system.collections.specialized.stringcollection?view=netcore-3.1) . En este ejemplo se da por supuesto que ya ha cargado la lista de palabras del disco y ha creado una colección StringCollection a partir de estas palabras.


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
> La propiedad [**Strokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes) del objeto [**RecognizerContext**](inkrecognizercontext-class.md) debe estar vacía antes de establecer la propiedad de la cadena de [**palabras**](inkwordlist-class.md) . Si la propiedad [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) no está vacía, se produce una excepción. Además, las palabras nunca se deben agregar a una lista de palabras una vez que se han asignado a un objeto **RecognizerContext** . Las palabras que se agregan a la lista de palabras después de asignarlas al objeto **RecognizerContext** no se actualizan en el reconocedor. Para actualizar la lista de palabras, debe reasignar el objeto de lista de **palabras** a la propiedad de lista de [**palabras**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) del objeto **RecognizerContext** .

 

Para obtener la máxima precisión del reconocimiento, combine Factoids con el Diccionario de aplicación en una relación ventajosa. Para obtener más información sobre la relación entre Factoids y los diccionarios de aplicación, vea [Descripción de las listas de palabras, el contexto del reconocedor y Factoids](understanding-wordlists--the-recognizercontext--and-factoids.md).

Para obtener un ejemplo del uso de diccionarios de aplicación con el control [InkEdit](inkedit-control-reference.md) , consulte [uso de un diccionario de aplicación con InkEdit](using-an-application-dictionary-with-inkedit.md).

 

 
