---
title: THEME. openDialog
description: El método openDialog abre un cuadro de diálogo de archivo.
ms.assetid: d7f4549c-a5c3-4902-b13b-51f3d4444ea9
keywords:
- Media Player de Windows de THEME. openDialog
topic_type:
- apiref
api_name:
- THEME.openDialog
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 79b9478b6b970b1d8d18b6f40975479e4755fa6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700424"
---
# <a name="themeopendialog"></a><span data-ttu-id="49702-104">THEME. openDialog</span><span class="sxs-lookup"><span data-stu-id="49702-104">THEME.openDialog</span></span>

<span data-ttu-id="49702-105">El método **openDialog** abre un cuadro de diálogo de archivo.</span><span class="sxs-lookup"><span data-stu-id="49702-105">The **openDialog** method opens a file dialog box.</span></span>

``` syntax
        theme.openDialog(dialogType, parameters)
```

## <a name="parameters"></a><span data-ttu-id="49702-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="49702-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49702-107"><span id="dialogType"></span><span id="dialogtype"></span><span id="DIALOGTYPE"></span>*dialogType*</span><span class="sxs-lookup"><span data-stu-id="49702-107"><span id="dialogType"></span><span id="dialogtype"></span><span id="DIALOGTYPE"></span>*dialogType*</span></span>
</dt> <dd>

<span data-ttu-id="49702-108">**Cadena** que especifica el tipo de cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="49702-108">A **String** that specifies the type of dialog box.</span></span> <span data-ttu-id="49702-109">Debe establecerse en "archivo \_ Abrir".</span><span class="sxs-lookup"><span data-stu-id="49702-109">Must be set to "FILE\_OPEN".</span></span>

</dd> <dt>

<span data-ttu-id="49702-110"><span id="parameters"></span><span id="PARAMETERS"></span>*los*</span><span class="sxs-lookup"><span data-stu-id="49702-110"><span id="parameters"></span><span id="PARAMETERS"></span>*parameters*</span></span>
</dt> <dd>

<span data-ttu-id="49702-111">**Cadena** que se puede utilizar para obtener información adicional.</span><span class="sxs-lookup"><span data-stu-id="49702-111">A **String** that can be used for additional information.</span></span> <span data-ttu-id="49702-112">Debe establecerse en "archivos \_ ALLMEDIA".</span><span class="sxs-lookup"><span data-stu-id="49702-112">Must be set to "FILES\_ALLMEDIA".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49702-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="49702-113">Return Value</span></span>

<span data-ttu-id="49702-114">Este método devuelve una **cadena** que contiene la dirección URL del archivo seleccionado o "" (cadena vacía) si el usuario hace clic en Cancelar.</span><span class="sxs-lookup"><span data-stu-id="49702-114">This method returns a **String** containing the URL of the selected file or "" (empty string) if the user clicks cancel.</span></span>

## <a name="remarks"></a><span data-ttu-id="49702-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="49702-115">Remarks</span></span>

<span data-ttu-id="49702-116">Este método se puede usar para los archivos de las unidades de disco duro locales o de las unidades de red.</span><span class="sxs-lookup"><span data-stu-id="49702-116">This method can be used for files on the local hard drives or on network drives.</span></span>

## <a name="examples"></a><span data-ttu-id="49702-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="49702-117">Examples</span></span>


```JScript
<THEME>
  <VIEW id="View1" 
    backgroundImage="greenstone.bmp" 
    width=500 height=300 author="Microsoft Corp.">
    <BUTTON 
      id="Open" 
      image="Open.png" 
      onclick="jscript:
        player.URL = theme.openDialog('FILE_OPEN','FILES_ALLMEDIA')">
    </BUTTON>
  </VIEW>
</THEME>
```



## <a name="requirements"></a><span data-ttu-id="49702-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49702-118">Requirements</span></span>



| <span data-ttu-id="49702-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="49702-119">Requirement</span></span> | <span data-ttu-id="49702-120">Value</span><span class="sxs-lookup"><span data-stu-id="49702-120">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="49702-121">Versión</span><span class="sxs-lookup"><span data-stu-id="49702-121">Version</span></span><br/> | <span data-ttu-id="49702-122">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="49702-122">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="49702-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="49702-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49702-124">**Elemento THEME**</span><span class="sxs-lookup"><span data-stu-id="49702-124">**THEME Element**</span></span>](theme-element.md)
</dt> </dl>

 

 





