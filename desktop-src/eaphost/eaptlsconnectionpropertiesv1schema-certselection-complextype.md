---
title: Tipo complejo de CertSelection
description: Obtenga información sobre el tipo complejo de CertSelection. Este tipo determina el modo en que el usuario selecciona un certificado.
ms.assetid: f5a37258-8ab0-4736-9721-6c2800769c74
keywords:
- Tipo complejo CertSelection EAPHost
topic_type:
- apiref
api_name:
- CertSelection
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ba22df8dca61696f214e495542319168183dd2bf
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104359420"
---
# <a name="certselection-complex-type"></a><span data-ttu-id="3b36e-105">Tipo complejo de CertSelection</span><span class="sxs-lookup"><span data-stu-id="3b36e-105">CertSelection Complex Type</span></span>

<span data-ttu-id="3b36e-106">El tipo complejo de **CertSelection** determina el modo en que el usuario selecciona un certificado.</span><span class="sxs-lookup"><span data-stu-id="3b36e-106">The **CertSelection** complex type determines how the user selects a certificate.</span></span>

``` syntax
<xs:complexType name="CertSelection">
    <xs:sequence>
        <xs:element name="SimpleCertSelection"
            type="boolean"
            minOccurs="0"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="3b36e-107">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3b36e-107">Child elements</span></span>



| <span data-ttu-id="3b36e-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="3b36e-108">Element</span></span>                                                                                                     | <span data-ttu-id="3b36e-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="3b36e-109">Type</span></span>    | <span data-ttu-id="3b36e-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="3b36e-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3b36e-111">**SimpleCertSelection**</span><span class="sxs-lookup"><span data-stu-id="3b36e-111">**SimpleCertSelection**</span></span>](eaptlsconnectionpropertiesv1schema-simplecertselection-certselection-element.md) | <span data-ttu-id="3b36e-112">boolean</span><span class="sxs-lookup"><span data-stu-id="3b36e-112">boolean</span></span> | <span data-ttu-id="3b36e-113">Es TRUE de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="3b36e-113">Is TRUE by default.</span></span> <span data-ttu-id="3b36e-114">Si [**SimpleCertSelection**](eaptlsconnectionpropertiesv1schema-simplecertselection-certselection-element.md) es true, EAP-TLS realiza una búsqueda de certificados simple sin ninguna lista desplegable para la selección de certificados.</span><span class="sxs-lookup"><span data-stu-id="3b36e-114">If [**SimpleCertSelection**](eaptlsconnectionpropertiesv1schema-simplecertselection-certselection-element.md) is TRUE, EAP-TLS performs a simple certificate search without any drop-down lists for the selection of certificates.</span></span> <span data-ttu-id="3b36e-115">Si **SimpleCertSelection** es false, EAP-TLS muestra al usuario el certificado adecuado que se va a seleccionar.</span><span class="sxs-lookup"><span data-stu-id="3b36e-115">If **SimpleCertSelection** is FALSE, EAP-TLS illustrates to the user the suitable certificate to be selected.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="3b36e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b36e-116">Requirements</span></span>



| <span data-ttu-id="3b36e-117">Role</span><span class="sxs-lookup"><span data-stu-id="3b36e-117">Role</span></span> | <span data-ttu-id="3b36e-118">Versión mínima admitida del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="3b36e-118">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="3b36e-119">Remoto</span><span class="sxs-lookup"><span data-stu-id="3b36e-119">Client</span></span><br/> | <span data-ttu-id="3b36e-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3b36e-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3b36e-121">Servidor</span><span class="sxs-lookup"><span data-stu-id="3b36e-121">Server</span></span><br/> | <span data-ttu-id="3b36e-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3b36e-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3b36e-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b36e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b36e-124">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="3b36e-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="3b36e-125">Esquema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="3b36e-125">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="3b36e-126">Tipos complejos de esquema de eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="3b36e-126">eaptlsconnectionpropertiesv1 Schema Complex Types</span></span>](eaptlsconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 





