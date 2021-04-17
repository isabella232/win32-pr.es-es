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
# <a name="using-application-dictionaries-with-the-tablet-pc-platform-apis"></a><span data-ttu-id="33499-103">Uso de diccionarios de aplicación con las API de la plataforma de Tablet PC</span><span class="sxs-lookup"><span data-stu-id="33499-103">Using Application Dictionaries with the Tablet PC Platform APIs</span></span>

<span data-ttu-id="33499-104">Para usar un diccionario de aplicación con la API de Tablet PC, primero debe crear un archivo con la lista de palabras del Diccionario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="33499-104">To use an application dictionary with the Tablet PC API, you must first create a file with the list of words for your application dictionary.</span></span>

<span data-ttu-id="33499-105">La solución más sencilla es usar un archivo de texto que contenga una lista de las palabras.</span><span class="sxs-lookup"><span data-stu-id="33499-105">The easiest solution for this is to use a text file that contains a list of the words.</span></span> <span data-ttu-id="33499-106">Cuando se carga la aplicación, lee el archivo de texto y crea [**un objeto**](inkwordlist-class.md) de lista de palabras a partir de la lista de palabras del archivo.</span><span class="sxs-lookup"><span data-stu-id="33499-106">When your application loads, it reads the text file and creates a [**WordList**](inkwordlist-class.md) object from the list of words in the file.</span></span> <span data-ttu-id="33499-107">Para cada [**RecognizerContext**](inkrecognizercontext-class.md) asociado al Diccionario de aplicación, establezca la propiedad lista de [**palabras**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) del objeto **RecognizerContext** en la lista de palabras del archivo de texto.</span><span class="sxs-lookup"><span data-stu-id="33499-107">For each [**RecognizerContext**](inkrecognizercontext-class.md) associated with the application dictionary, set the [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) property of the **RecognizerContext** object to the word list in the text file.</span></span>

<span data-ttu-id="33499-108">En el ejemplo siguiente se muestra cómo crear un objeto de una colección de [**palabras**](inkwordlist-class.md) a partir de una colección [StringCollection](/dotnet/api/system.collections.specialized.stringcollection?view=netcore-3.1) .</span><span class="sxs-lookup"><span data-stu-id="33499-108">The following example illustrates how to create a [**WordList**](inkwordlist-class.md) object from a [StringCollection](/dotnet/api/system.collections.specialized.stringcollection?view=netcore-3.1) collection.</span></span> <span data-ttu-id="33499-109">En este ejemplo se da por supuesto que ya ha cargado la lista de palabras del disco y ha creado una colección StringCollection a partir de estas palabras.</span><span class="sxs-lookup"><span data-stu-id="33499-109">This example assumes that you have already loaded the list of words from disk and created a StringCollection collection from these words.</span></span>


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
> <span data-ttu-id="33499-110">La propiedad [**Strokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes) del objeto [**RecognizerContext**](inkrecognizercontext-class.md) debe estar vacía antes de establecer la propiedad de la cadena de [**palabras**](inkwordlist-class.md) .</span><span class="sxs-lookup"><span data-stu-id="33499-110">The [**Strokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes) property of the [**RecognizerContext**](inkrecognizercontext-class.md) object must be empty before you set the [**WordList**](inkwordlist-class.md) property.</span></span> <span data-ttu-id="33499-111">Si la propiedad [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) no está vacía, se produce una excepción.</span><span class="sxs-lookup"><span data-stu-id="33499-111">If the [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) property is not empty, an exception is thrown.</span></span> <span data-ttu-id="33499-112">Además, las palabras nunca se deben agregar a una lista de palabras una vez que se han asignado a un objeto **RecognizerContext** .</span><span class="sxs-lookup"><span data-stu-id="33499-112">In addition, words should never be added to a word list after it has been assigned to a **RecognizerContext** object.</span></span> <span data-ttu-id="33499-113">Las palabras que se agregan a la lista de palabras después de asignarlas al objeto **RecognizerContext** no se actualizan en el reconocedor.</span><span class="sxs-lookup"><span data-stu-id="33499-113">Words that are added to the word list after it is assigned to the **RecognizerContext** object are not updated in the recognizer.</span></span> <span data-ttu-id="33499-114">Para actualizar la lista de palabras, debe reasignar el objeto de lista de **palabras** a la propiedad de lista de [**palabras**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) del objeto **RecognizerContext** .</span><span class="sxs-lookup"><span data-stu-id="33499-114">To update the word list you must reassign the **WordList** object to the [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) property of the **RecognizerContext** object.</span></span>

 

<span data-ttu-id="33499-115">Para obtener la máxima precisión del reconocimiento, combine Factoids con el Diccionario de aplicación en una relación ventajosa.</span><span class="sxs-lookup"><span data-stu-id="33499-115">For maximum recognition accuracy, combine factoids with your application dictionary in an advantageous relationship.</span></span> <span data-ttu-id="33499-116">Para obtener más información sobre la relación entre Factoids y los diccionarios de aplicación, vea [Descripción de las listas de palabras, el contexto del reconocedor y Factoids](understanding-wordlists--the-recognizercontext--and-factoids.md).</span><span class="sxs-lookup"><span data-stu-id="33499-116">For more information about the relationship between factoids and application dictionaries, see [Understanding Word Lists, Recognizer Context, and Factoids](understanding-wordlists--the-recognizercontext--and-factoids.md).</span></span>

<span data-ttu-id="33499-117">Para obtener un ejemplo del uso de diccionarios de aplicación con el control [InkEdit](inkedit-control-reference.md) , consulte [uso de un diccionario de aplicación con InkEdit](using-an-application-dictionary-with-inkedit.md).</span><span class="sxs-lookup"><span data-stu-id="33499-117">For an example of using application dictionaries with the [InkEdit](inkedit-control-reference.md) control, see [Using an Application Dictionary with InkEdit](using-an-application-dictionary-with-inkedit.md).</span></span>

 

 
