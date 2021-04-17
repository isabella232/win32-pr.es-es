---
description: El método DVDAdm. ConfirmPassword comprueba si la contraseña especificada coincide con la contraseña guardada previamente.
ms.assetid: 4dddc28d-edf7-45a2-ae1f-1c37b5df2eea
title: Método ConfirmPassword (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62817247ca661f92ceb5ba0e2bc9bb11381d73ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670985"
---
# <a name="confirmpassword-method"></a><span data-ttu-id="9042a-103">Método ConfirmPassword</span><span class="sxs-lookup"><span data-stu-id="9042a-103">ConfirmPassword Method</span></span>

> [!Note]  
> <span data-ttu-id="9042a-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="9042a-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="9042a-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="9042a-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="9042a-106">El `DVDAdm.ConfirmPassword` método comprueba si la contraseña especificada coincide con la contraseña guardada previamente.</span><span class="sxs-lookup"><span data-stu-id="9042a-106">The `DVDAdm.ConfirmPassword` method tests whether the specified password matches the previously saved password.</span></span>

``` syntax
[ bIsConfirmed = ] DVD.DVDAdm.ConfirmPassword(sUserName, sPassword)
```

## <a name="parameters"></a><span data-ttu-id="9042a-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9042a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9042a-108"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span><span class="sxs-lookup"><span data-stu-id="9042a-108"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span></span>
</dt> <dd>

<span data-ttu-id="9042a-109">Especifica el nombre del usuario como una cadena.</span><span class="sxs-lookup"><span data-stu-id="9042a-109">Specifies the user's name as a String.</span></span>

</dd> <dt>

<span data-ttu-id="9042a-110"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span><span class="sxs-lookup"><span data-stu-id="9042a-110"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span></span>
</dt> <dd>

<span data-ttu-id="9042a-111">Especifica la nueva contraseña como una cadena.</span><span class="sxs-lookup"><span data-stu-id="9042a-111">Specifies the new password as a String.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9042a-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9042a-112">Return Value</span></span>

<span data-ttu-id="9042a-113">Devuelve true si la contraseña especificada coincide con la contraseña existente; de lo contrario, devuelve false.</span><span class="sxs-lookup"><span data-stu-id="9042a-113">Returns true if the specified password matches the existing password, false otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9042a-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9042a-114">Remarks</span></span>

<span data-ttu-id="9042a-115">Actualmente, el parámetro *sUserName* se omite en este y todos los métodos relacionados.</span><span class="sxs-lookup"><span data-stu-id="9042a-115">Currently, the *sUserName* parameter is ignored on this and all related methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="9042a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9042a-116">Requirements</span></span>



| <span data-ttu-id="9042a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9042a-117">Requirement</span></span> | <span data-ttu-id="9042a-118">Value</span><span class="sxs-lookup"><span data-stu-id="9042a-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9042a-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9042a-119">Header</span></span><br/> | <dl> <span data-ttu-id="9042a-120"><dt>Segmento. h</dt></span><span class="sxs-lookup"><span data-stu-id="9042a-120"><dt>Segment.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9042a-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="9042a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9042a-122">**ChangePassword**</span><span class="sxs-lookup"><span data-stu-id="9042a-122">**ChangePassword**</span></span>](changepassword-method.md)
</dt> <dt>

[<span data-ttu-id="9042a-123">Objeto MSDVDAdm</span><span class="sxs-lookup"><span data-stu-id="9042a-123">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 




