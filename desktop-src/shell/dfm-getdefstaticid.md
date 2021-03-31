---
description: Enviado por la implementación predeterminada del menú contextual durante la creación, especificando el comando de menú predeterminado y permitiendo realizar una elección alternativa. Usado por LPFNDFMCALLBACK.
title: Mensaje de DFM_GETDEFSTATICID (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9e4ad96e-7c90-456e-8668-21b347f2915c
api_name:
- DFM_GETDEFSTATICID
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3fb1635b624b4c39e91ad8c31645c9aad598c7fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423708"
---
# <a name="dfm_getdefstaticid-message"></a><span data-ttu-id="4c9f9-104">DFM \_ GETDEFSTATICID</span><span class="sxs-lookup"><span data-stu-id="4c9f9-104">DFM\_GETDEFSTATICID message</span></span>

<span data-ttu-id="4c9f9-105">Enviado por la implementación predeterminada del menú contextual durante la creación, especificando el comando de menú predeterminado y permitiendo realizar una elección alternativa.</span><span class="sxs-lookup"><span data-stu-id="4c9f9-105">Sent by the default context menu implementation during creation, specifying the default menu command and allowing an alternate choice to be made.</span></span> <span data-ttu-id="4c9f9-106">Usado por [**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback).</span><span class="sxs-lookup"><span data-stu-id="4c9f9-106">Used by [**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback).</span></span>


```C++
DFM_GETDEFSTATICID
    lParam = (LPARAM)(int*) defaultID;          
            
```



## <a name="parameters"></a><span data-ttu-id="4c9f9-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4c9f9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c9f9-108">*defaultID* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="4c9f9-108">*defaultID* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4c9f9-109">Puntero al identificador del comando de menú seleccionado.</span><span class="sxs-lookup"><span data-stu-id="4c9f9-109">A pointer to the ID of the selected menu command.</span></span> <span data-ttu-id="4c9f9-110">Se reconoce la siguiente marca.</span><span class="sxs-lookup"><span data-stu-id="4c9f9-110">The following flag is recognized.</span></span>

<dt>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>

<span data-ttu-id="4c9f9-111"><span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**propiedades de DFM \_ cmd \_**</span><span class="sxs-lookup"><span data-stu-id="4c9f9-111"><span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**DFM\_CMD\_PROPERTIES**</span></span>


</dt> <dd>

<span data-ttu-id="4c9f9-112">Muestra la interfaz de usuario de **propiedades** del elemento en el que se invocó el menú.</span><span class="sxs-lookup"><span data-stu-id="4c9f9-112">Show the **Properties** UI for the item the menu was invoked on.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4c9f9-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4c9f9-113">Remarks</span></span>

<span data-ttu-id="4c9f9-114">Para invalidar la opción predeterminada del comando, el controlador debería, tras la recepción de este mensaje, establecer el valor señalado por *defaultID* en el identificador del comando de reemplazo y devolver S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="4c9f9-114">To override the default command choice, your handler should, upon receipt of this message, set the value pointed to by *defaultID* to the ID of the replacement command and return S\_OK.</span></span> <span data-ttu-id="4c9f9-115">Devuelve un código de error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="4c9f9-115">Return a failure code otherwise.</span></span>

<span data-ttu-id="4c9f9-116">Este mensaje se envía a la función de devolución de llamada o al objeto de devolución de llamada, dependiendo de cómo se construya el objeto de menú contextual predeterminado.</span><span class="sxs-lookup"><span data-stu-id="4c9f9-116">This message is sent to either the callback function or the callback object depending on how the default context menu object is constructed.</span></span> <span data-ttu-id="4c9f9-117">Hay dos API para su construcción, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span><span class="sxs-lookup"><span data-stu-id="4c9f9-117">There are two APIs for its construction, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span>

<span data-ttu-id="4c9f9-118">[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) es una versión extendida de este mensaje y proporciona más información a la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="4c9f9-118">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="4c9f9-119">Use **DFM \_ INVOKECOMMANDEX** si necesita la información adicional proporcionada por esa interfaz en su implementación de.</span><span class="sxs-lookup"><span data-stu-id="4c9f9-119">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c9f9-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c9f9-120">Requirements</span></span>



| <span data-ttu-id="4c9f9-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c9f9-121">Requirement</span></span> | <span data-ttu-id="4c9f9-122">Value</span><span class="sxs-lookup"><span data-stu-id="4c9f9-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4c9f9-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4c9f9-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4c9f9-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4c9f9-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="4c9f9-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4c9f9-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4c9f9-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4c9f9-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4c9f9-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4c9f9-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c9f9-128"><dt>ShlObj. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c9f9-128"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
