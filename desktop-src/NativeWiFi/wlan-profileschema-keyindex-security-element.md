---
description: Especifica qué índice de clave se debe usar para cifrar el tráfico inalámbrico. Solo se utiliza cuando keyType está establecido en &\# 0034; networkKey&\# 0034;.
ms.assetid: 5629605d-4c23-4318-8f09-939e13302552
title: Elemento keyIndex (Security)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- keyIndex
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 43bb802d46abb3c4684b63206377d3464078e2c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156784"
---
# <a name="keyindex-security-element"></a><span data-ttu-id="032ae-104">Elemento keyIndex (Security)</span><span class="sxs-lookup"><span data-stu-id="032ae-104">keyIndex (security) Element</span></span>

<span data-ttu-id="032ae-105">El elemento keyIndex (Security) especifica qué índice de clave se debe usar para cifrar el tráfico inalámbrico.</span><span class="sxs-lookup"><span data-stu-id="032ae-105">The keyIndex (security) element specifies which key index should be used to encrypt wireless traffic.</span></span> <span data-ttu-id="032ae-106">Solo se utiliza cuando [**KeyType**](wlan-profileschema-keytype-sharedkey-element.md) está establecido en "networkKey".</span><span class="sxs-lookup"><span data-stu-id="032ae-106">This is only used when [**keyType**](wlan-profileschema-keytype-sharedkey-element.md) is set to "networkKey".</span></span>

``` syntax
<xs:element name="keyIndex"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:minInclusive
                value="0"
             />
            <xs:maxInclusive
                value="3"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="032ae-107">El elemento se define mediante el elemento de [**seguridad**](wlan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="032ae-107">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="032ae-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="032ae-108">Requirements</span></span>



| <span data-ttu-id="032ae-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="032ae-109">Requirement</span></span> | <span data-ttu-id="032ae-110">Value</span><span class="sxs-lookup"><span data-stu-id="032ae-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="032ae-111">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="032ae-111">Minimum supported client</span></span><br/> | <span data-ttu-id="032ae-112">Windows Vista, Windows XP con SP3 \[ solo aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="032ae-112">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="032ae-113">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="032ae-113">Minimum supported server</span></span><br/> | <span data-ttu-id="032ae-114">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="032ae-114">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="032ae-115">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="032ae-115">Redistributable</span></span><br/>          | <span data-ttu-id="032ae-116">API de LAN inalámbrica para Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="032ae-116">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="032ae-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="032ae-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="032ae-118">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="032ae-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="032ae-119">**bursátil**</span><span class="sxs-lookup"><span data-stu-id="032ae-119">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="032ae-120">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="032ae-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="032ae-121">**seguridad (MSM)**</span><span class="sxs-lookup"><span data-stu-id="032ae-121">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




