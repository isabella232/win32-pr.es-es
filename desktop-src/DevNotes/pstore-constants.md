---
description: PStore usa las siguientes constantes.
ms.assetid: 4bdccb86-2e0e-461c-9a74-184861b7db1e
title: PStore (constantes) (pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_E_OK
- PST_E_TYPE_EXISTS
- PST_AUTHENTICODE
- PST_BINARY_CHECK
- PST_SECURITY_DESCRIPTOR
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: 1c80fe7235a859ef0a754420fe5bd22caa10d6bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670869"
---
# <a name="pstore-constants"></a><span data-ttu-id="a11e9-103">PStore (constantes)</span><span class="sxs-lookup"><span data-stu-id="a11e9-103">PStore Constants</span></span>

<span data-ttu-id="a11e9-104">\[El almacenamiento protegido (pstore) está disponible para su uso en Windows Server 2003 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a11e9-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="a11e9-105">Solo está disponible para las operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en las versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="a11e9-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="a11e9-106">Pstore usa una implementación anterior de la protección de datos.</span><span class="sxs-lookup"><span data-stu-id="a11e9-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="a11e9-107">Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura proporcionada por las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="a11e9-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="a11e9-108">PStore usa las siguientes constantes.</span><span class="sxs-lookup"><span data-stu-id="a11e9-108">The following constants are used by PStore.</span></span>

<span data-ttu-id="a11e9-109">Códigos de error de almacenamiento protegido</span><span class="sxs-lookup"><span data-stu-id="a11e9-109">Protected Storage Error Codes</span></span>



| <span data-ttu-id="a11e9-110">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="a11e9-110">Constant/value</span></span>                                                                                                                                                                                                                               | <span data-ttu-id="a11e9-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="a11e9-111">Description</span></span>                                                        |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| <span id="PST_E_OK"></span><span id="pst_e_ok"></span><dl> <span data-ttu-id="a11e9-112"><dt>**Archivo pst \_ E \_ Aceptar**</dt> <dt>0x00000000L</dt></span><span class="sxs-lookup"><span data-stu-id="a11e9-112"><dt>**PST\_E\_OK**</dt> <dt>0x00000000L</dt></span></span> </dl>                             | <span data-ttu-id="a11e9-113">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="a11e9-113">The operation was successful.</span></span><br/>                           |
| <span id="PST_E_TYPE_EXISTS"></span><span id="pst_e_type_exists"></span><dl> <span data-ttu-id="a11e9-114"><dt>**Archivo pst \_ El \_ tipo E \_ existe**</dt> <dt>0x800C0004L</dt></span><span class="sxs-lookup"><span data-stu-id="a11e9-114"><dt>**PST\_E\_TYPE\_EXISTS**</dt> <dt>0x800C0004L</dt></span></span> </dl> | <span data-ttu-id="a11e9-115">El elemento de datos ya existe en el almacenamiento protegido.</span><span class="sxs-lookup"><span data-stu-id="a11e9-115">The data item already exists in the protected storage.</span></span> <br/> |



<span data-ttu-id="a11e9-116">Valores de la cláusula de acceso</span><span class="sxs-lookup"><span data-stu-id="a11e9-116">Access Clause Values</span></span>



| <span data-ttu-id="a11e9-117">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="a11e9-117">Constant/value</span></span>                                                                                                                                                                                                                                      | <span data-ttu-id="a11e9-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="a11e9-118">Description</span></span>                                                                             |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| <span id="PST_AUTHENTICODE"></span><span id="pst_authenticode"></span><dl> <span data-ttu-id="a11e9-119"><dt>**Archivo pst \_ AUTHENTICODE**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a11e9-119"><dt>**PST\_AUTHENTICODE**</dt> <dt>1</dt></span></span> </dl>                       | <span data-ttu-id="a11e9-120">Apunta a una estructura de [**\_ AUTHENTICODEDATA de PST**](pst-authenticodedata.md) .</span><span class="sxs-lookup"><span data-stu-id="a11e9-120">Points to a [**PST\_AUTHENTICODEDATA**](pst-authenticodedata.md) structure.</span></span><br/> |
| <span id="PST_BINARY_CHECK_"></span><span id="pst_binary_check_"></span><dl> <span data-ttu-id="a11e9-121"><dt> **\_ \_ Comprobación binaria de PST**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a11e9-121"><dt>**PST\_BINARY\_CHECK** </dt> <dt>2</dt></span></span> </dl>                   | <span data-ttu-id="a11e9-122">Apunta a una estructura de **\_ BINARYCHECKDATA de PST** .</span><span class="sxs-lookup"><span data-stu-id="a11e9-122">Points to a **PST\_BINARYCHECKDATA** structure.</span></span><br/>                              |
| <span id="PST_SECURITY_DESCRIPTOR"></span><span id="pst_security_descriptor"></span><dl> <span data-ttu-id="a11e9-123"><dt>**Archivo pst \_ \_Descriptor de seguridad**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="a11e9-123"><dt>**PST\_SECURITY\_DESCRIPTOR**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="a11e9-124">Apunta a un descriptor de seguridad de Windows válido.</span><span class="sxs-lookup"><span data-stu-id="a11e9-124">Points to a valid Windows security descriptor.</span></span> <br/>                              |



## <a name="requirements"></a><span data-ttu-id="a11e9-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a11e9-125">Requirements</span></span>



| <span data-ttu-id="a11e9-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a11e9-126">Requirement</span></span> | <span data-ttu-id="a11e9-127">Value</span><span class="sxs-lookup"><span data-stu-id="a11e9-127">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a11e9-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a11e9-128">Header</span></span><br/> | <dl> <span data-ttu-id="a11e9-129"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="a11e9-129"><dt>Pstore.h</dt></span></span> </dl> |



 

 
