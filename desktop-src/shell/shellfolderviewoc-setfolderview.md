---
description: Reenvía los eventos del objeto ShellFolderView especificado al controlador de eventos ShellFolderViewOC correspondiente.
ms.assetid: 44a2a0a5-aa87-43ae-b4ea-0d301fcb8464
title: Método ShellFolderViewOC. SetFolderView (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderViewOC.SetFolderView
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 7d331fadbd8abae62ee896caec772d84d079f88d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985871"
---
# <a name="shellfolderviewocsetfolderview-method"></a><span data-ttu-id="1c866-103">ShellFolderViewOC. SetFolderView, método</span><span class="sxs-lookup"><span data-stu-id="1c866-103">ShellFolderViewOC.SetFolderView method</span></span>

<span data-ttu-id="1c866-104">Reenvía los eventos del objeto [**ShellFolderView**](shellfolderview.md) especificado al controlador de eventos [**ShellFolderViewOC**](shellfolderviewoc-object.md) correspondiente.</span><span class="sxs-lookup"><span data-stu-id="1c866-104">Forwards the events of the specified [**ShellFolderView**](shellfolderview.md) object to the corresponding [**ShellFolderViewOC**](shellfolderviewoc-object.md) event handler.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c866-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1c866-105">Syntax</span></span>


```JScript
iRetVal = ShellFolderViewOC.SetFolderView(
  oShellFolderView
)
```



## <a name="parameters"></a><span data-ttu-id="1c866-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1c866-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c866-107">*oShellFolderView* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1c866-107">*oShellFolderView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c866-108">Tipo: \**[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) \** _</span><span class="sxs-lookup"><span data-stu-id="1c866-108">Type: \**[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\** _</span></span>

<span data-ttu-id="1c866-109">Un objeto [_ *ShellFolderView* \*](shellfolderview.md) .</span><span class="sxs-lookup"><span data-stu-id="1c866-109">A [_ *ShellFolderView*\*](shellfolderview.md) object.</span></span> <span data-ttu-id="1c866-110">Sus eventos [**EnumDone**](shellfolderviewoc-enumdone.md) y [**SelectionChanged**](shellfolderview-selectionchanged.md) se reenviarán al controlador de eventos [**ShellFolderViewOC**](shellfolderviewoc-object.md) correspondiente.</span><span class="sxs-lookup"><span data-stu-id="1c866-110">Its [**EnumDone**](shellfolderviewoc-enumdone.md) and [**SelectionChanged**](shellfolderview-selectionchanged.md) events will be forwarded to the corresponding [**ShellFolderViewOC**](shellfolderviewoc-object.md) event handler.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1c866-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c866-111">Requirements</span></span>



| <span data-ttu-id="1c866-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c866-112">Requirement</span></span> | <span data-ttu-id="1c866-113">Value</span><span class="sxs-lookup"><span data-stu-id="1c866-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c866-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1c866-114">Minimum supported client</span></span><br/> | <span data-ttu-id="1c866-115">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="1c866-115">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1c866-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1c866-116">Minimum supported server</span></span><br/> | <span data-ttu-id="1c866-117">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1c866-117">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="1c866-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1c866-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c866-119"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c866-119"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="1c866-120">IDL</span><span class="sxs-lookup"><span data-stu-id="1c866-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1c866-121"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1c866-121"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="1c866-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1c866-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c866-123"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="1c866-123"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
