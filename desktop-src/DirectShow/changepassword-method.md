---
description: El método DVDAdm. ChangePassword guarda una nueva contraseña de aplicación en el registro.
ms.assetid: 58dac785-e20e-4a41-89cf-56644964da19
title: ChangePassword (método)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bba8bfb9adcecdb88f19f3ac1b8061f93486e269
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494525"
---
# <a name="changepassword-method"></a><span data-ttu-id="932b0-103">ChangePassword (método)</span><span class="sxs-lookup"><span data-stu-id="932b0-103">ChangePassword Method</span></span>

> [!Note]  
> <span data-ttu-id="932b0-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="932b0-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="932b0-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="932b0-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="932b0-106">El `DVDAdm.ChangePassword` método guarda una nueva contraseña de aplicación en el registro.</span><span class="sxs-lookup"><span data-stu-id="932b0-106">The `DVDAdm.ChangePassword` method saves a new application password in the registry.</span></span>

``` syntax
        DVD.DVDAdm.ChangePassword(sUserName, sOld, sNew)
```

## <a name="parameters"></a><span data-ttu-id="932b0-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="932b0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="932b0-108"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span><span class="sxs-lookup"><span data-stu-id="932b0-108"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span></span>
</dt> <dd>

<span data-ttu-id="932b0-109">Especifica el nombre de inicio de sesión del usuario actual como una cadena.</span><span class="sxs-lookup"><span data-stu-id="932b0-109">Specifies the current user's logon name as a String.</span></span> <span data-ttu-id="932b0-110">El objeto MSDVDAdm omite este parámetro.</span><span class="sxs-lookup"><span data-stu-id="932b0-110">The MSDVDAdm object ignores this parameter.</span></span> <span data-ttu-id="932b0-111">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="932b0-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="932b0-112"><span id="sOld"></span><span id="sold"></span><span id="SOLD"></span>*Venda*</span><span class="sxs-lookup"><span data-stu-id="932b0-112"><span id="sOld"></span><span id="sold"></span><span id="SOLD"></span>*sOld*</span></span>
</dt> <dd>

<span data-ttu-id="932b0-113">Especifica la contraseña anterior del usuario como una cadena.</span><span class="sxs-lookup"><span data-stu-id="932b0-113">Specifies the user's old password as a String.</span></span>

</dd> <dt>

<span data-ttu-id="932b0-114"><span id="sNew"></span><span id="snew"></span><span id="SNEW"></span>*sNew*</span><span class="sxs-lookup"><span data-stu-id="932b0-114"><span id="sNew"></span><span id="snew"></span><span id="SNEW"></span>*sNew*</span></span>
</dt> <dd>

<span data-ttu-id="932b0-115">Especifica la nueva contraseña del usuario como una cadena.</span><span class="sxs-lookup"><span data-stu-id="932b0-115">Specifies the user's new password as a String.</span></span> <span data-ttu-id="932b0-116">No puede ser una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="932b0-116">Cannot be an empty string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="932b0-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="932b0-117">Return Value</span></span>

<span data-ttu-id="932b0-118">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="932b0-118">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="932b0-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="932b0-119">Remarks</span></span>

<span data-ttu-id="932b0-120">Actualmente, el parámetro *sUserName* se omite en este y todos los métodos relacionados.</span><span class="sxs-lookup"><span data-stu-id="932b0-120">Currently, the *sUserName* parameter is ignored on this and all related methods.</span></span> <span data-ttu-id="932b0-121">Esto significa que quien sabe que la contraseña puede establecer el nivel parental.</span><span class="sxs-lookup"><span data-stu-id="932b0-121">This means that whoever knows the password can set the parental level.</span></span> <span data-ttu-id="932b0-122">Solo hay una contraseña y un nivel parental para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="932b0-122">There is only one password and one parental level for the application.</span></span> <span data-ttu-id="932b0-123">No se admiten nombres de inicio de sesión de usuario individuales ni administración de varias contraseñas.</span><span class="sxs-lookup"><span data-stu-id="932b0-123">There is no support for individual user logon names or multiple password management.</span></span> <span data-ttu-id="932b0-124">Para aplicar los niveles de administración parental, los padres deben establecer la contraseña y, a continuación, establecer el nivel parental adecuado para los miembros jóvenes del grupo de familiares.</span><span class="sxs-lookup"><span data-stu-id="932b0-124">To enforce parental management levels, parents should set the password and then set the parental level appropriate for younger members of the group of relatives.</span></span> <span data-ttu-id="932b0-125">Cuando los padres quieren ver un disco con contenido clasificado por adultos, pueden cambiar el nivel y, a continuación, cambiarlo de nuevo cuando hayan terminado de verlo.</span><span class="sxs-lookup"><span data-stu-id="932b0-125">When parents want to view a disc with adult-rated content, they can change the level, and then change it back when they are done viewing.</span></span> <span data-ttu-id="932b0-126">Siempre que los elementos secundarios no conozcan la contraseña, solo podrán ver el contenido en el nivel establecido o debajo de él.</span><span class="sxs-lookup"><span data-stu-id="932b0-126">As long as the children do not know the password, they can only watch content at or below the level set for them.</span></span>

## <a name="see-also"></a><span data-ttu-id="932b0-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="932b0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="932b0-128">**ConfirmPassword**</span><span class="sxs-lookup"><span data-stu-id="932b0-128">**ConfirmPassword**</span></span>](confirmpassword-method.md)
</dt> <dt>

[<span data-ttu-id="932b0-129">Objeto MSDVDAdm</span><span class="sxs-lookup"><span data-stu-id="932b0-129">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



