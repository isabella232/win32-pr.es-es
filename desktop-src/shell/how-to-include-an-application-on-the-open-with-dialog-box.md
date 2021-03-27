---
description: Muestra cómo asegurarse de que la aplicación aparece en el menú y el cuadro de diálogo Abrir con para aplicaciones de escritorio, y que está disponible como una aplicación de la tienda Windows predeterminada para los tipos de archivo especificados.
ms.assetid: DFCC07A6-BED5-41A8-86DC-130082AE665A
title: Cómo incluir una aplicación en el cuadro de diálogo Abrir con
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 218dcbfe6dc34770208c017f0e13cfda7686430c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909541"
---
# <a name="how-to-include-an-application-in-the-open-with-dialog-box"></a><span data-ttu-id="e733b-103">Cómo incluir una aplicación en el cuadro de diálogo Abrir con</span><span class="sxs-lookup"><span data-stu-id="e733b-103">How to Include an Application in the Open With Dialog Box</span></span>

<span data-ttu-id="e733b-104">Muestra cómo asegurarse de que la aplicación aparece en el menú y el cuadro de diálogo **abrir con** para aplicaciones de escritorio, y que está disponible como una aplicación de la tienda Windows predeterminada para los tipos de archivo especificados.</span><span class="sxs-lookup"><span data-stu-id="e733b-104">Illustrates how to ensure your application appears in the **Open With** menu and dialog box for desktop apps, and is available as a default Windows Store app for specified file types.</span></span>

## <a name="instructions"></a><span data-ttu-id="e733b-105">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="e733b-105">Instructions</span></span>

### <a name="for-each-file-type-add-your-application-to-the-openwithprogids-registry-subkey"></a><span data-ttu-id="e733b-106">Para cada tipo de archivo, agregue la aplicación a la subclave del registro OpenWithProgIds.</span><span class="sxs-lookup"><span data-stu-id="e733b-106">For each file type, add your application to the OpenWithProgIds registry subkey.</span></span>

<span data-ttu-id="e733b-107">Agregue el ProgID como un nombre de valor, con el tipo de valor de REG \_ None o REG \_ SZ y una cadena vacía como valor de datos.</span><span class="sxs-lookup"><span data-stu-id="e733b-107">Add your ProgID as a value name, with the value type of either REG\_NONE or REG\_SZ and an empty string as the data value.</span></span>

<span data-ttu-id="e733b-108">Los siguientes ejemplos del registro muestran entradas que asocian InfoPath y Microsoft Visual Studio con el tipo de archivo XML.</span><span class="sxs-lookup"><span data-stu-id="e733b-108">The following registry examples show entries associating InfoPath and for Microsoft Visual Studio with the XML file type.</span></span>

```
HKEY_CLASSES_ROOT
   .xml
      OpenWithProgids
         InfoPath.Document.3 REG_SZ
         VisualStudio.xml.10.0 REG_SZ
```

## <a name="remarks"></a><span data-ttu-id="e733b-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e733b-109">Remarks</span></span>

<span data-ttu-id="e733b-110">Se prefiere la subclave **OpenWithProgids** a **OpenWithList** para identificar una aplicación.</span><span class="sxs-lookup"><span data-stu-id="e733b-110">The **OpenWithProgids** subkey is preferred to **OpenWithList** to identify an application.</span></span> <span data-ttu-id="e733b-111">Para obtener más información sobre estas subclaves, vea [configuración de subclaves opcionales y atributos de extensión de tipo de archivo](fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="e733b-111">For more information on these subkeys, see [Setting Optional Subkeys and File Type Extension Attributes](fa-file-types.md).</span></span>

<span data-ttu-id="e733b-112">**OpenWithList** está pensado únicamente para aplicaciones heredadas (debe ser. exe solamente) en sistemas operativos anteriores a Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e733b-112">**OpenWithList** is intended only for legacy apps (must be .exe only) on operating systems prior to Windows XP.</span></span>

```
HKEY_CLASSES_ROOT
   .xml
      OpenWithList
         AlternateProgram1.exe
         AlternateProgram2.exe
```

 

 



