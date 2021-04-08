---
title: UI_PKEY_Keytip
description: Identifica la \_ propiedad KeyTip PKEY de la interfaz de usuario \_ .
ms.assetid: 7af4abcb-abb0-466a-bc58-274fa18b79af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 550bfac9b341d14b495c73e4426e8143d91d8e19
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994295"
---
# <a name="ui_pkey_keytip"></a><span data-ttu-id="9e3bc-103">KeyTip de UI \_ PKEY \_</span><span class="sxs-lookup"><span data-stu-id="9e3bc-103">UI\_PKEY\_Keytip</span></span>

<span data-ttu-id="9e3bc-104">Identifica la \_ propiedad KeyTip PKEY de la interfaz de usuario \_ .</span><span class="sxs-lookup"><span data-stu-id="9e3bc-104">Identifies the UI\_PKEY\_Keytip property.</span></span>

```
propertyDescription
   name = UI_PKEY_Keytip
   shellPKey = UI_PKEY_Keytip
   formatID = 00000003-7363-696e-8441798acf5aebb7
   propID = 3
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a><span data-ttu-id="9e3bc-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9e3bc-105">Remarks</span></span>

<span data-ttu-id="9e3bc-106">\_ \_ Una aplicación usa KeyTip de PKEY de IU para consultar la tecla de aceleración de un control de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="9e3bc-106">UI\_PKEY\_Keytip is used by an application to query the keyboard accelerator of a ribbon control.</span></span>

<span data-ttu-id="9e3bc-107">Este valor de propiedad es una cadena, que se compone de cualquier secuencia de caracteres, incluido el espacio en blanco.</span><span class="sxs-lookup"><span data-stu-id="9e3bc-107">This property value is a string, composed of any sequence of characters including white space.</span></span>

<span data-ttu-id="9e3bc-108">El valor de KeyTip de UI \_ PKEY \_ actúa como la tecla de aceleración para un comando, a menos que ese comando se exponga a través de un elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="9e3bc-108">The value of UI\_PKEY\_Keytip acts as the keyboard accelerator for a Command unless that Command is exposed through a menu item.</span></span> <span data-ttu-id="9e3bc-109">En este caso, el marco de trabajo omite el valor de KeyTip PKEY de la interfaz de usuario \_ \_ y, en su lugar, usa un carácter precedido por una y comercial según lo especificado por el [**comando. LabelTitle**](windowsribbon-element-command-labeltitle.md) o la [ \_ \_ etiqueta PKEY](windowsribbon-reference-properties-uipkey-label.md)de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="9e3bc-109">In this case, the framework ignores the UI\_PKEY\_Keytip value and instead uses a character preceded by an ampersand as specified by [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) or [UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md).</span></span> <span data-ttu-id="9e3bc-110">Si no se especifica el carácter de y comercial mediante la etiqueta **Command. LabelTitle** o UI \_ PKEY \_ , no se expone ningún KeyTip ni tecla de aceleración.</span><span class="sxs-lookup"><span data-stu-id="9e3bc-110">If no ampersand is specified by **Command.LabelTitle** or UI\_PKEY\_Label, no keytip or keyboard accelerator is exposed.</span></span>

<span data-ttu-id="9e3bc-111">La longitud máxima de KeyTip de PKEY de la interfaz de usuario \_ \_ no está enlazada.</span><span class="sxs-lookup"><span data-stu-id="9e3bc-111">The maximum length of UI\_PKEY\_Keytip is unbounded.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9e3bc-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9e3bc-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e3bc-113">Propiedades de recursos</span><span class="sxs-lookup"><span data-stu-id="9e3bc-113">Resource Properties</span></span>](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[<span data-ttu-id="9e3bc-114">**Command. KeyTip**</span><span class="sxs-lookup"><span data-stu-id="9e3bc-114">**Command.Keytip**</span></span>](windowsribbon-element-command-keytip.md)
</dt> </dl>

 

 




