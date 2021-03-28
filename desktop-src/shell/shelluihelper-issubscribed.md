---
description: Indica si se ha suscrito a una dirección URL especificada.
title: Método ShellUIHelper. IsSubscribed (exdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper.IsSubscribed
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: fcf23352-6603-4b17-9c3b-b353cca1c003
ms.openlocfilehash: 2085f38e5f91f13a2f67ff4f22b003b533249386
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082809"
---
# <a name="shelluihelperissubscribed-method"></a><span data-ttu-id="03a8d-103">ShellUIHelper. IsSubscribed, método</span><span class="sxs-lookup"><span data-stu-id="03a8d-103">ShellUIHelper.IsSubscribed method</span></span>

<span data-ttu-id="03a8d-104">Indica si se ha suscrito a una dirección URL especificada.</span><span class="sxs-lookup"><span data-stu-id="03a8d-104">Indicates whether a specified URL is subscribed to.</span></span>

## <a name="syntax"></a><span data-ttu-id="03a8d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="03a8d-105">Syntax</span></span>


```JScript
bRetVal = ShellUIHelper.IsSubscribed(
  sURL
)
```



## <a name="parameters"></a><span data-ttu-id="03a8d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="03a8d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03a8d-107">*sURL* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="03a8d-107">*sURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03a8d-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="03a8d-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="03a8d-109">Valor de **cadena** que especifica la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="03a8d-109">A **String** value that specifies the URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03a8d-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="03a8d-110">Return value</span></span>

<span data-ttu-id="03a8d-111">Tipo: \**booleano \** _</span><span class="sxs-lookup"><span data-stu-id="03a8d-111">Type: \**Boolean\** _</span></span>

<span data-ttu-id="03a8d-112">_ *true*\* si la dirección URL está suscrita a; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="03a8d-112">_ *true*\* if the URL is subscribed to; otherwise, **false**.</span></span>

## <a name="examples"></a><span data-ttu-id="03a8d-113">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="03a8d-113">Examples</span></span>

<span data-ttu-id="03a8d-114">En el ejemplo siguiente se muestra el uso correcto de este método para JScript incrustado en HTML y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="03a8d-114">The following example shows the proper usage of this method for JScript embedded in HTML and Visual Basic.</span></span>

<span data-ttu-id="03a8d-115">JScript.net</span><span class="sxs-lookup"><span data-stu-id="03a8d-115">JScript:</span></span>


```JScript
<html>
<head>
<title></title>

<object id="ShellUIHelper"
        classid="CLSID:64AB4BB7-111E-11d1-8F79-00C04FC2FBE1"
        width=0
        height=0
        VIEWASTEXT>
</object>

<script language="JavaScript">
    function fnShellUIHelperIsSubscribedJ()
    {
        var bReturn;
        
        bReturn = ShellUIHelper.IsSubscribed("https://www.microsoft.com/");
        alert(bReturn);
    }
</script>

</head>
<body onload=fnShellUIHelperIsSubscribedJ()>
</body>
</html>
```



<span data-ttu-id="03a8d-116">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="03a8d-116">Visual Basic:</span></span>


```VB
Private Sub fnShellUIHelperIsSubscribedVB()
    Dim objShellUIHelper As ShellUIHelper
    Dim bReturn          As Boolean
    
    Set objShellUIHelper = New ShellUIHelper
        bReturn = objShellUIHelper.IsSubscribed("https://www.microsoft.com/")
        Debug.Print bReturn
    Set objShellUIHelper = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="03a8d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03a8d-117">Requirements</span></span>



| <span data-ttu-id="03a8d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="03a8d-118">Requirement</span></span> | <span data-ttu-id="03a8d-119">Value</span><span class="sxs-lookup"><span data-stu-id="03a8d-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03a8d-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="03a8d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="03a8d-121">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="03a8d-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="03a8d-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="03a8d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="03a8d-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="03a8d-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="03a8d-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="03a8d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="03a8d-125"><dt>Exdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="03a8d-125"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="03a8d-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="03a8d-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03a8d-127"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="03a8d-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
