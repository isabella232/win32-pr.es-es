---
description: Agrega un nuevo canal a la lista de canales en el menú Favoritos de Windows Internet Explorer y en la barra Canal del escritorio.
title: Método ShellUIHelper.AddChannel (Exdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper.AddChannel
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b62e6e82-429a-4d41-96d4-cba639b611f5
ms.openlocfilehash: d08c1360cb2a96fbc7b87daecb650bbf46aa6ad9
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841206"
---
# <a name="shelluihelperaddchannel-method"></a><span data-ttu-id="1e08b-103">Método ShellUIHelper.AddChannel</span><span class="sxs-lookup"><span data-stu-id="1e08b-103">ShellUIHelper.AddChannel method</span></span>

<span data-ttu-id="1e08b-104">Agrega un nuevo canal a la lista de **canales** del menú Internet Explorer Favoritos de Windows y a la barra **Canal** del escritorio.</span><span class="sxs-lookup"><span data-stu-id="1e08b-104">Adds a new channel to the list of channels in the Windows Internet Explorer **Favorites** menu and to the **Channel** bar on the desktop.</span></span>

> [!Note]  
> <span data-ttu-id="1e08b-105">Este método ya no se admite en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1e08b-105">This method is no longer supported under Windows Vista.</span></span> <span data-ttu-id="1e08b-106">En ese sistema operativo, devuelve E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="1e08b-106">Under that operating system, it returns E\_NOTIMPL.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="1e08b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1e08b-107">Syntax</span></span>


```JScript
iRetVal = ShellUIHelper.AddChannel(
  sURL
)
```



## <a name="parameters"></a><span data-ttu-id="1e08b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1e08b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e08b-109">*sURL* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="1e08b-109">*sURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e08b-110">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="1e08b-110">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="1e08b-111">Valor **string** que especifica la dirección URL del archivo CDF.</span><span class="sxs-lookup"><span data-stu-id="1e08b-111">A **String** value that specifies the URL of the CDF file.</span></span>

> [!Note]  
> <span data-ttu-id="1e08b-112">Los vínculos del archivo CDF deben usar protocolos HTTP, HTTPS o FTP.</span><span class="sxs-lookup"><span data-stu-id="1e08b-112">The links in the CDF file must use HTTP, HTTPS, or FTP protocols.</span></span> <span data-ttu-id="1e08b-113">Si el archivo CDF contiene cualquier otro protocolo, se produce un error en la adición del canal y no aparece ningún cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="1e08b-113">If the CDF file contains any other protocol, the addition of the channel fails and no dialog box appears.</span></span>

 

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="1e08b-114">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="1e08b-114">Examples</span></span>

<span data-ttu-id="1e08b-115">En el ejemplo siguiente se muestra el uso adecuado de este método para JScript insertado en HTML y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="1e08b-115">The following example shows the proper usage of this method for JScript embedded in HTML and Visual Basic.</span></span>

<span data-ttu-id="1e08b-116">Jscript:</span><span class="sxs-lookup"><span data-stu-id="1e08b-116">JScript:</span></span>


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
    function fnShellUIHelperAddChannelJ()
    {
        ShellUIHelper.AddChannel("https://www.microsoft.com/windows/cdf/g_stock.cdf");
    }
</script>

</head>
<body onload=fnShellUIHelperAddChannelJ()>
</body>
</html>
```



<span data-ttu-id="1e08b-117">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="1e08b-117">Visual Basic:</span></span>


```VB
Private Sub fnShellUIHelperAddChannelVB()
    Dim objShellUIHelper As ShellUIHelper
    
    Set objShellUIHelper = New ShellUIHelper
        objShellUIHelper.AddChannel ("https://www.microsoft.com/windows/cdf/g_stock.cdf")
    Set objShellUIHelper = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="1e08b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e08b-118">Requirements</span></span>



| <span data-ttu-id="1e08b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e08b-119">Requirement</span></span> | <span data-ttu-id="1e08b-120">Value</span><span class="sxs-lookup"><span data-stu-id="1e08b-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e08b-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e08b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1e08b-122">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="1e08b-122">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="1e08b-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e08b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1e08b-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1e08b-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1e08b-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1e08b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e08b-126"><dt>Exdisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="1e08b-126"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="1e08b-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1e08b-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e08b-128"><dt>Shell32.dll (versión 4.71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="1e08b-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
