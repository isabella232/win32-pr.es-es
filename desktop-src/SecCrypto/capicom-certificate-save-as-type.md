---
description: Define el formato de un archivo que contiene información del certificado.
ms.assetid: 417a6d1b-6329-418c-823c-d82b94207fd6
title: Enumeración CAPICOM_CERTIFICATE_SAVE_AS_TYPE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERTIFICATE_SAVE_AS_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 1e5365594a5a1cf1f06691c63b37c04f38530575
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670855"
---
# <a name="capicom_certificate_save_as_type-enumeration"></a><span data-ttu-id="7fadf-103">\_ \_ \_ Enumeración de tipo guardar certificado de CAPICOM \_</span><span class="sxs-lookup"><span data-stu-id="7fadf-103">CAPICOM\_CERTIFICATE\_SAVE\_AS\_TYPE enumeration</span></span>

<span data-ttu-id="7fadf-104">El tipo de enumeración de **certificado de CAPICOM de \_ \_ tipo "Save \_ as \_** " define el formato de un archivo que contiene información del certificado.</span><span class="sxs-lookup"><span data-stu-id="7fadf-104">The **CAPICOM\_CERTIFICATE\_SAVE\_AS\_TYPE** enumeration type defines the format of a file containing certificate information.</span></span> <span data-ttu-id="7fadf-105">CAPICOM 2,0 presentó este tipo de enumeración.</span><span class="sxs-lookup"><span data-stu-id="7fadf-105">This enumeration type was introduced by CAPICOM 2.0.</span></span>

## <a name="members"></a><span data-ttu-id="7fadf-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="7fadf-106">Members</span></span>



| <span data-ttu-id="7fadf-107">Miembro</span><span class="sxs-lookup"><span data-stu-id="7fadf-107">Member</span></span>                                  | <span data-ttu-id="7fadf-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="7fadf-108">Description</span></span>                                                                                                                                   | <span data-ttu-id="7fadf-109">Value</span><span class="sxs-lookup"><span data-stu-id="7fadf-109">Value</span></span> |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="7fadf-110">**el \_ certificado \_ de CAPICOM se guarda \_ como \_ pfx**</span><span class="sxs-lookup"><span data-stu-id="7fadf-110">**CAPICOM\_CERTIFICATE\_SAVE\_AS\_PFX**</span></span> | <span data-ttu-id="7fadf-111">El archivo de salida se formateará como archivo PFX (PKCS 12) y también se guardarán las claves privadas asociadas que se puedan exportar.</span><span class="sxs-lookup"><span data-stu-id="7fadf-111">The output file will be formatted as a PFX (PKCS 12) file and any associated private keys which are exportable will also be saved.</span></span><br/> | <span data-ttu-id="7fadf-112">0</span><span class="sxs-lookup"><span data-stu-id="7fadf-112">0</span></span>     |
| <span data-ttu-id="7fadf-113">**\_certificado \_ de CAPICOM guardar \_ como \_ cer**</span><span class="sxs-lookup"><span data-stu-id="7fadf-113">**CAPICOM\_CERTIFICATE\_SAVE\_AS\_CER**</span></span> | <span data-ttu-id="7fadf-114">El archivo de salida se formateará como un archivo CER sin ninguna clave privada guardada.</span><span class="sxs-lookup"><span data-stu-id="7fadf-114">The output file will be formatted as a CER file with no private keys saved.</span></span><br/>                                                        | <span data-ttu-id="7fadf-115">1</span><span class="sxs-lookup"><span data-stu-id="7fadf-115">1</span></span>     |



## <a name="remarks"></a><span data-ttu-id="7fadf-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7fadf-116">Remarks</span></span>

<span data-ttu-id="7fadf-117">El método [**Certificate. Save**](certificate-save.md) usa el tipo de enumeración de **\_ \_ \_ \_ tipo guardar certificado de CAPICOM** .</span><span class="sxs-lookup"><span data-stu-id="7fadf-117">The **CAPICOM\_CERTIFICATE\_SAVE\_AS\_TYPE** enumeration type is used by the [**Certificate.Save**](certificate-save.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fadf-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7fadf-118">Requirements</span></span>



| <span data-ttu-id="7fadf-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fadf-119">Requirement</span></span> | <span data-ttu-id="7fadf-120">Value</span><span class="sxs-lookup"><span data-stu-id="7fadf-120">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7fadf-121">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="7fadf-121">Redistributable</span></span><br/> | <span data-ttu-id="7fadf-122">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="7fadf-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="7fadf-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7fadf-123">Header</span></span><br/>          | <dl> <span data-ttu-id="7fadf-124"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fadf-124"><dt>Capicom.h</dt></span></span> </dl> |



 

 




