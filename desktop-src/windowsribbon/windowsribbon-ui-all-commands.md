---
title: UI_ALL_COMMANDS (Uiribbon. h)
description: Especifica una constante que identifica la colección de comandos declarada en el archivo de recursos de marcado.
ms.assetid: b0046d8c-bb54-4231-90f0-c0b2c8790b1a
topic_type:
- apiref
api_name:
- UI_ALL_COMMANDS
api_location:
- Uiribbon.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cce287d6ee03734ecbb0dd84e020ec542a83f04b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714560"
---
# <a name="ui_all_commands"></a><span data-ttu-id="fb69a-103">comandos de UI \_ All \_</span><span class="sxs-lookup"><span data-stu-id="fb69a-103">UI\_ALL\_COMMANDS</span></span>

<span data-ttu-id="fb69a-104">Especifica una constante que identifica la colección de comandos declarada en el archivo de recursos de marcado.</span><span class="sxs-lookup"><span data-stu-id="fb69a-104">Specifies a constant that identifies the collection of Commands declared in the Markup resource file.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb69a-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fb69a-105">Remarks</span></span>

<span data-ttu-id="fb69a-106">**Interfaz de usuario \_ Todos los \_ comandos** resultan útiles cuando es necesario tener acceso a propiedades similares en todos los comandos.</span><span class="sxs-lookup"><span data-stu-id="fb69a-106">**UI\_ALL\_COMMANDS** is useful when it is necessary to access similar properties across all Commands.</span></span> <span data-ttu-id="fb69a-107">Por ejemplo, la **interfaz de usuario \_ todos los \_ comandos** se pueden pasar a [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) para invalidar y actualizar todos los comandos de la cinta de opciones mediante la consulta de nuevos valores de propiedad en la aplicación host.</span><span class="sxs-lookup"><span data-stu-id="fb69a-107">For example, **UI\_ALL\_COMMANDS** can be passed to [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) to invalidate and refresh all Ribbon Commands by querying the host application for new property values.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb69a-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb69a-108">Requirements</span></span>



| <span data-ttu-id="fb69a-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb69a-109">Requirement</span></span> | <span data-ttu-id="fb69a-110">Value</span><span class="sxs-lookup"><span data-stu-id="fb69a-110">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb69a-111">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb69a-111">Minimum supported client</span></span><br/> | <span data-ttu-id="fb69a-112">Windows 7, Windows Vista con SP2 y actualización de plataforma solo para aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="fb69a-112">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="fb69a-113">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb69a-113">Minimum supported server</span></span><br/> | <span data-ttu-id="fb69a-114">Windows Server 2008 R2, Windows Server 2008 con SP2 y actualización de plataforma solo para aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="fb69a-114">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="fb69a-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fb69a-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb69a-116"><dt>Uiribbon. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb69a-116"><dt>Uiribbon.h</dt></span></span> </dl>                                             |
| <span data-ttu-id="fb69a-117">IDL</span><span class="sxs-lookup"><span data-stu-id="fb69a-117">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fb69a-118"><dt>Uiribbon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fb69a-118"><dt>Uiribbon.idl</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="fb69a-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="fb69a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb69a-120">Constantes y enumeraciones</span><span class="sxs-lookup"><span data-stu-id="fb69a-120">Constants and Enumerations</span></span>](windowsribbon-reference-enumerations.md)
</dt> </dl>

 

