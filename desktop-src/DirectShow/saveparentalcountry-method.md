---
description: El método DVDAdm. SaveParentalCountry guarda el nuevo país o región parental de la aplicación en el registro.
ms.assetid: 2185ad7d-c7c1-4d8b-82e7-5ed5fffaff26
title: Método SaveParentalCountry (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9ca47a6ca10f25298b4eb10fdcf532c8d764b96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690481"
---
# <a name="saveparentalcountry-method"></a><span data-ttu-id="a7ecb-103">Método SaveParentalCountry</span><span class="sxs-lookup"><span data-stu-id="a7ecb-103">SaveParentalCountry Method</span></span>

> [!Note]  
> <span data-ttu-id="a7ecb-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a7ecb-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="a7ecb-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="a7ecb-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="a7ecb-106">El `DVDAdm.SaveParentalCountry` método guarda el nuevo país o región parental de la aplicación en el registro.</span><span class="sxs-lookup"><span data-stu-id="a7ecb-106">The `DVDAdm.SaveParentalCountry` method saves the application's new parental country/region to the registry.</span></span>

``` syntax
DVD.DVDAdm.SaveParentalCountry(iCountry, sUserName, sPassword)
```

## <a name="parameters"></a><span data-ttu-id="a7ecb-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a7ecb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7ecb-108"><span id="iCountry"></span><span id="icountry"></span><span id="ICOUNTRY"></span>*iCountry*</span><span class="sxs-lookup"><span data-stu-id="a7ecb-108"><span id="iCountry"></span><span id="icountry"></span><span id="ICOUNTRY"></span>*iCountry*</span></span>
</dt> <dd>

<span data-ttu-id="a7ecb-109">Especifica el país o la región parental como un entero.</span><span class="sxs-lookup"><span data-stu-id="a7ecb-109">Specifies the parental country/region as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="a7ecb-110"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span><span class="sxs-lookup"><span data-stu-id="a7ecb-110"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span></span>
</dt> <dd>

<span data-ttu-id="a7ecb-111">Especifica el nombre de usuario como una cadena.</span><span class="sxs-lookup"><span data-stu-id="a7ecb-111">Specifies the user name as a String.</span></span> <span data-ttu-id="a7ecb-112">(Actualmente omitido).</span><span class="sxs-lookup"><span data-stu-id="a7ecb-112">(Currently ignored.)</span></span>

</dd> <dt>

<span data-ttu-id="a7ecb-113"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span><span class="sxs-lookup"><span data-stu-id="a7ecb-113"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span></span>
</dt> <dd>

<span data-ttu-id="a7ecb-114">Especifica la contraseña como una cadena.</span><span class="sxs-lookup"><span data-stu-id="a7ecb-114">Specifies the password as a String.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7ecb-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a7ecb-115">Return value</span></span>

<span data-ttu-id="a7ecb-116">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="a7ecb-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7ecb-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a7ecb-117">Remarks</span></span>

<span data-ttu-id="a7ecb-118">Este método permite a un usuario que conoce la contraseña actual guardar en el registro un nuevo valor de país o región parental.</span><span class="sxs-lookup"><span data-stu-id="a7ecb-118">This method enables a user who knows the current password to save a new parental country/region setting to the registry.</span></span> <span data-ttu-id="a7ecb-119">Al igual que con todos los métodos de **MSDVDAdm**, este método no afecta al nivel actual del reproductor; solo cambia la configuración del registro, de modo que la próxima vez que se cree el objeto MSWebDVD, se abrirá con el nuevo país o región.</span><span class="sxs-lookup"><span data-stu-id="a7ecb-119">As with all the methods of **MSDVDAdm**, this method does not affect the current level in the player; it changes only the registry setting, so that the next time the MSWebDVD object is created, it will open with the new country/region.</span></span> <span data-ttu-id="a7ecb-120">Para cambiar el país o la región parental en el reproductor, llame a [**SelectParentalCountry**](selectparentalcountry-method.md), que no cambia la configuración del registro.</span><span class="sxs-lookup"><span data-stu-id="a7ecb-120">To change the parental country/region in the player, call [**SelectParentalCountry**](selectparentalcountry-method.md), which does not change the registry setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7ecb-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7ecb-121">Requirements</span></span>



| <span data-ttu-id="a7ecb-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7ecb-122">Requirement</span></span> | <span data-ttu-id="a7ecb-123">Value</span><span class="sxs-lookup"><span data-stu-id="a7ecb-123">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a7ecb-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a7ecb-124">Header</span></span><br/> | <dl> <span data-ttu-id="a7ecb-125"><dt>Segmento. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7ecb-125"><dt>Segment.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7ecb-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="a7ecb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7ecb-127">**SaveParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="a7ecb-127">**SaveParentalLevel**</span></span>](saveparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="a7ecb-128">Objeto MSDVDAdm</span><span class="sxs-lookup"><span data-stu-id="a7ecb-128">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 




