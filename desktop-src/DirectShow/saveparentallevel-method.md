---
description: El método DVDAdm. SaveParentalLevel guarda un nuevo nivel de parental predeterminado en el registro.
ms.assetid: 8ad22098-acbd-41fd-9224-829b3cc5f8ae
title: Método SaveParentalLevel (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94d30d26264dff077de391b6b513f7e9ab5048c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680300"
---
# <a name="saveparentallevel-method"></a><span data-ttu-id="4226a-103">Método SaveParentalLevel</span><span class="sxs-lookup"><span data-stu-id="4226a-103">SaveParentalLevel Method</span></span>

> [!Note]  
> <span data-ttu-id="4226a-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="4226a-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="4226a-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="4226a-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="4226a-106">El método **DVDAdm. SaveParentalLevel** guarda un nuevo nivel de parental predeterminado en el registro.</span><span class="sxs-lookup"><span data-stu-id="4226a-106">The **DVDAdm.SaveParentalLevel** method saves a new default parental level to the registry.</span></span>

``` syntax
DVD.DVDAdm.SaveParentalLevel(iLevel, sUserName, sPassword)
```

## <a name="parameters"></a><span data-ttu-id="4226a-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4226a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4226a-108"><span id="iLevel"></span><span id="ilevel"></span><span id="ILEVEL"></span>*iLevel*</span><span class="sxs-lookup"><span data-stu-id="4226a-108"><span id="iLevel"></span><span id="ilevel"></span><span id="ILEVEL"></span>*iLevel*</span></span>
</dt> <dd>

<span data-ttu-id="4226a-109">Especifica el nivel de parental como valor de entero de 1 a 8.</span><span class="sxs-lookup"><span data-stu-id="4226a-109">Specifies the parental level as anInteger value from 1 through 8.</span></span>

</dd> <dt>

<span data-ttu-id="4226a-110"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span><span class="sxs-lookup"><span data-stu-id="4226a-110"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span></span>
</dt> <dd>

<span data-ttu-id="4226a-111">Especifica el nombre de usuario como una cadena.</span><span class="sxs-lookup"><span data-stu-id="4226a-111">Specifies the user name as a String.</span></span> <span data-ttu-id="4226a-112">(Actualmente omitido).</span><span class="sxs-lookup"><span data-stu-id="4226a-112">(Currently ignored.)</span></span>

</dd> <dt>

<span data-ttu-id="4226a-113"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span><span class="sxs-lookup"><span data-stu-id="4226a-113"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span></span>
</dt> <dd>

<span data-ttu-id="4226a-114">Especifica la contraseña como una cadena.</span><span class="sxs-lookup"><span data-stu-id="4226a-114">Specifies the password as a String.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4226a-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4226a-115">Return Value</span></span>

<span data-ttu-id="4226a-116">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="4226a-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4226a-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4226a-117">Remarks</span></span>

<span data-ttu-id="4226a-118">Este método permite a un usuario que conoce la contraseña actual guardar una nueva configuración de nivel parental en el registro.</span><span class="sxs-lookup"><span data-stu-id="4226a-118">This method enables a user who knows the current password to save a new parental level setting to the registry.</span></span> <span data-ttu-id="4226a-119">Al igual que con todos los métodos de **MSDVDAdm**, este método no afecta al nivel actual del reproductor; solo cambia la configuración del registro, de modo que la próxima vez que se inicie el objeto MSWebDVD, se abrirá con el nuevo nivel.</span><span class="sxs-lookup"><span data-stu-id="4226a-119">As with all the methods of **MSDVDAdm**, this method does not affect the current level in the player; it changes only the registry setting, so that the next time the MSWebDVD object is started, it will open with the new level.</span></span> <span data-ttu-id="4226a-120">Especifique-1 para deshabilitar la administración parental.</span><span class="sxs-lookup"><span data-stu-id="4226a-120">Specify -1 to disable parental management.</span></span> <span data-ttu-id="4226a-121">Para cambiar el nivel parental en el reproductor, llame a [**SelectParentalLevel**](selectparentallevel-method.md), que no cambia la configuración del registro.</span><span class="sxs-lookup"><span data-stu-id="4226a-121">To change the parental level in the player, call [**SelectParentalLevel**](selectparentallevel-method.md), which does not change the registry setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="4226a-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4226a-122">Requirements</span></span>



| <span data-ttu-id="4226a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4226a-123">Requirement</span></span> | <span data-ttu-id="4226a-124">Value</span><span class="sxs-lookup"><span data-stu-id="4226a-124">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4226a-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4226a-125">Header</span></span><br/> | <dl> <span data-ttu-id="4226a-126"><dt>Segmento. h</dt></span><span class="sxs-lookup"><span data-stu-id="4226a-126"><dt>Segment.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4226a-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="4226a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4226a-128">Objeto MSDVDAdm</span><span class="sxs-lookup"><span data-stu-id="4226a-128">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 




