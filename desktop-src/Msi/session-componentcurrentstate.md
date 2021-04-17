---
description: La propiedad ComponentCurrentState del objeto de sesión es una propiedad de solo lectura que devuelve el estado instalado actual del componente designado. Para los valores de estado, consulte la propiedad ComponentRequestState.
ms.assetid: c8343e90-8867-462d-9844-e547341a590c
title: Propiedad Session. ComponentCurrentState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.ComponentCurrentState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8c556dd9656ebced155ef90fe96abd394a32ff1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653704"
---
# <a name="sessioncomponentcurrentstate-property"></a><span data-ttu-id="c7495-104">Propiedad Session. ComponentCurrentState</span><span class="sxs-lookup"><span data-stu-id="c7495-104">Session.ComponentCurrentState property</span></span>

<span data-ttu-id="c7495-105">La propiedad **ComponentCurrentState** del objeto de [**sesión**](session-object.md) es una propiedad de solo lectura que devuelve el estado instalado actual del componente designado.</span><span class="sxs-lookup"><span data-stu-id="c7495-105">The **ComponentCurrentState** property of the [**Session**](session-object.md) object is a read-only property that returns the current installed state of the designated component.</span></span> <span data-ttu-id="c7495-106">Para los valores de estado, consulte la propiedad [**ComponentRequestState**](session-componentrequeststate.md) .</span><span class="sxs-lookup"><span data-stu-id="c7495-106">For state values, see the [**ComponentRequestState**](session-componentrequeststate.md) property.</span></span>

<span data-ttu-id="c7495-107">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c7495-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7495-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c7495-108">Syntax</span></span>


```JScript
propVal = Session.ComponentCurrentState
```



## <a name="property-value"></a><span data-ttu-id="c7495-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="c7495-109">Property value</span></span>

<span data-ttu-id="c7495-110">Nombre de cadena requerido del componente solicitado, clave principal en la tabla de componentes.</span><span class="sxs-lookup"><span data-stu-id="c7495-110">Required string name of the requested component, primary key into the Component table.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7495-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c7495-111">Remarks</span></span>

<span data-ttu-id="c7495-112">Si se produce un error en la propiedad, puede obtener información de error extendida mediante el método [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="c7495-112">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7495-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7495-113">Requirements</span></span>



| <span data-ttu-id="c7495-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7495-114">Requirement</span></span> | <span data-ttu-id="c7495-115">Value</span><span class="sxs-lookup"><span data-stu-id="c7495-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7495-116">Versión</span><span class="sxs-lookup"><span data-stu-id="c7495-116">Version</span></span><br/> | <span data-ttu-id="c7495-117">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c7495-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c7495-118">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c7495-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c7495-119">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="c7495-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="c7495-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c7495-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="c7495-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7495-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="c7495-122">IID</span><span class="sxs-lookup"><span data-stu-id="c7495-122">IID</span></span><br/>     | <span data-ttu-id="c7495-123">El IID \_ ISession se define como 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="c7495-123">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



## <a name="see-also"></a><span data-ttu-id="c7495-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="c7495-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7495-125">**De sesión**</span><span class="sxs-lookup"><span data-stu-id="c7495-125">**Session**</span></span>](session-object.md)
</dt> <dt>

[<span data-ttu-id="c7495-126">**Propiedad ComponentRequestState**</span><span class="sxs-lookup"><span data-stu-id="c7495-126">**ComponentRequestState property**</span></span>](session-componentrequeststate.md)
</dt> </dl>

 

 




