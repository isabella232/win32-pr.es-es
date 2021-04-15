---
description: Los dispositivos portátiles de Windows admiten las siguientes propiedades de Asociación de red.
ms.assetid: 5e1b3e8d-9620-4b68-b7ef-1642404ed6ed
title: Propiedades de la Asociación de red (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Network
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 41e40e456d4671d1aa8fb190274afd2f5ace98b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708910"
---
# <a name="network-association-properties"></a><span data-ttu-id="27305-103">Propiedades de la Asociación de red</span><span class="sxs-lookup"><span data-stu-id="27305-103">Network Association Properties</span></span>

<span data-ttu-id="27305-104">Los dispositivos portátiles de Windows admiten las siguientes propiedades de Asociación de red.</span><span class="sxs-lookup"><span data-stu-id="27305-104">Windows Portable Devices supports the following network association properties.</span></span>



| <span data-ttu-id="27305-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="27305-105">Property</span></span>                                                  | <span data-ttu-id="27305-106">VarType</span><span class="sxs-lookup"><span data-stu-id="27305-106">VarType</span></span>                   | <span data-ttu-id="27305-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="27305-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27305-108">**\_ \_ \_ \_ identificadores de red de host de Asociación de red de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="27305-108">**WPD\_NETWORK\_ASSOCIATION\_HOST\_NETWORK\_IDENTIFIERS**</span></span> | <span data-ttu-id="27305-109">**VT \_ Vector \| VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="27305-109">**VT\_VECTOR \| VT\_UI1**</span></span> | <span data-ttu-id="27305-110">Lista de identificadores de host EUI-64 válidos para esta asociación. Se trata de una matriz de bytes que contiene un número entero de direcciones de red física EUI-64.</span><span class="sxs-lookup"><span data-stu-id="27305-110">The list of EUI-64 host identifiers valid for this association.This is an array of bytes that contains an integral number of EUI-64 physical network addresses.</span></span> <span data-ttu-id="27305-111">Estos valores EUI-64 son las direcciones de red física disponibles en el host en el momento de la Asociación de red.</span><span class="sxs-lookup"><span data-stu-id="27305-111">These EUI-64 values are the physical network addresses available on the host at Network Association time.</span></span> <span data-ttu-id="27305-112">Si el host tiene direcciones de red física de MAC-48 (típico de redes IPv4), cada dirección MAC-48 se codificará en la dirección EUI-64 como las dos mitades de la dirección MAC-48 separadas por FF-FF.</span><span class="sxs-lookup"><span data-stu-id="27305-112">If the host has MAC-48 physical network addresses (typical of IPv4 networks), each MAC-48 address will be encoded in the EUI-64 address as the two halves of the MAC-48 address separated by FF-FF.</span></span><br/> |
| <span data-ttu-id="27305-113">**\_X509V3SEQUENCE de \_ Asociación de red de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="27305-113">**WPD\_NETWORK\_ASSOCIATION\_X509V3SEQUENCE**</span></span>             | <span data-ttu-id="27305-114">**VT \_ Vector \| VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="27305-114">**VT\_VECTOR \| VT\_UI1**</span></span> | <span data-ttu-id="27305-115">Secuencia de certificados X. 509 V3 que se va a proporcionar para la autenticación del servidor TLS.</span><span class="sxs-lookup"><span data-stu-id="27305-115">The sequence of X.509 v3 certificates to be provided for TLS server authentication.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="27305-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27305-116">Requirements</span></span>



| <span data-ttu-id="27305-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="27305-117">Requirement</span></span> | <span data-ttu-id="27305-118">Value</span><span class="sxs-lookup"><span data-stu-id="27305-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="27305-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="27305-119">Header</span></span><br/> | <dl> <span data-ttu-id="27305-120"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="27305-120"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27305-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="27305-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27305-122">**Propiedades y atributos de WPD**</span><span class="sxs-lookup"><span data-stu-id="27305-122">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




