---
description: Especifica el tamaño del bloque de bytes cifrado para el cifrado del modelo basado en el ejemplo.
ms.assetid: 1F370DEC-20B5-456D-BB68-C94E183410F3
title: MFSampleExtension_Encryption_CryptByteBlock atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 927e08d81cc8066f73b579c8abf419d754fc1713
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082436"
---
# <a name="mfsampleextension_encryption_cryptbyteblock-attribute"></a><span data-ttu-id="4f3e0-103">MFSampleExtension \_ Encryption \_ CryptByteBlock Attribute</span><span class="sxs-lookup"><span data-stu-id="4f3e0-103">MFSampleExtension\_Encryption\_CryptByteBlock attribute</span></span>

<span data-ttu-id="4f3e0-104">Especifica el tamaño del bloque de bytes cifrado para el cifrado del modelo basado en el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="4f3e0-104">Specifies the encrypted byte block size for sample-based pattern encryption.</span></span>

## <a name="data-type"></a><span data-ttu-id="4f3e0-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="4f3e0-105">Data type</span></span>

<span data-ttu-id="4f3e0-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="4f3e0-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="4f3e0-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4f3e0-107">Remarks</span></span>

<span data-ttu-id="4f3e0-108">El número de bytes claros (no cifrados) en el bloque de asignación de submuestra se especifica en el atributo [MFSampleExtension \_ Encryption \_ SkipByteBlock](mfsampleextension-encryption-skipbyteblock.md) .</span><span class="sxs-lookup"><span data-stu-id="4f3e0-108">The number of clear (non-encrypted) bytes in the subsample mapping block are specified in the [MFSampleExtension\_Encryption\_SkipByteBlock](mfsampleextension-encryption-skipbyteblock.md) attribute.</span></span> <span data-ttu-id="4f3e0-109">Si alguno de estos atributos no está presente o tiene un valor de 0, significa que los datos de ejemplo no están cifrados.</span><span class="sxs-lookup"><span data-stu-id="4f3e0-109">If either of these attributes are not present or have a value of 0, it means that the sample data is not encrypted.</span></span> <span data-ttu-id="4f3e0-110">Ninguno de estos valores debe ser distinto de cero, los valores positivos o ambos deben tener un valor de cero.</span><span class="sxs-lookup"><span data-stu-id="4f3e0-110">Either both of these values must be non-zero, positive values, or both must have a value of zero.</span></span>

<span data-ttu-id="4f3e0-111">En los casos en los que el origen está basado en MP4, el valor se establece en función de los valores del \_ bloque de bytes de cifrado predeterminado en \_ \_ el cuadro seguimiento de cifrado (' tenc ') en el encabezado MP4.</span><span class="sxs-lookup"><span data-stu-id="4f3e0-111">In cases where the Source is MP4-based, the value is set based off the values of default\_crypt\_byte\_block within the track encryption box (‘tenc’) in the MP4 header.</span></span> <span data-ttu-id="4f3e0-112">Para obtener más información, vea [MFSampleExtension \_ Encryption \_ ProtectionScheme](mfsampleextension-encryption-protectionscheme.md).</span><span class="sxs-lookup"><span data-stu-id="4f3e0-112">For more information, see [MFSampleExtension\_Encryption\_ProtectionScheme](mfsampleextension-encryption-protectionscheme.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4f3e0-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f3e0-113">Requirements</span></span>



| <span data-ttu-id="4f3e0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f3e0-114">Requirement</span></span> | <span data-ttu-id="4f3e0-115">Value</span><span class="sxs-lookup"><span data-stu-id="4f3e0-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4f3e0-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4f3e0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4f3e0-117">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="4f3e0-117">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="4f3e0-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4f3e0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4f3e0-119">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="4f3e0-119">None supported</span></span><br/>                                                          |
| <span data-ttu-id="4f3e0-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4f3e0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f3e0-121"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f3e0-121"><dt>Mfidl.h</dt></span></span> </dl> |



 

 




