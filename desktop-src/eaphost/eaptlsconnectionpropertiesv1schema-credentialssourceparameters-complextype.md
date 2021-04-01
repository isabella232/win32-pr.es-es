---
title: Tipo complejo de CredentialsSourceParameters
description: Define el elemento necesario para especificar el origen del certificado que se va a utilizar con una autenticación EAP-TLS.
ms.assetid: 1482694e-3025-4231-8154-4be0301fe5ce
keywords:
- Tipo complejo CredentialsSourceParameters EAPHost
topic_type:
- apiref
api_name:
- CredentialsSourceParameters
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 912faa4a388d9a57225991959625a978ca0921f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150682"
---
# <a name="credentialssourceparameters-complex-type"></a><span data-ttu-id="dca45-104">Tipo complejo de CredentialsSourceParameters</span><span class="sxs-lookup"><span data-stu-id="dca45-104">CredentialsSourceParameters Complex Type</span></span>

<span data-ttu-id="dca45-105">El tipo complejo **CredentialsSourceParameters** define el elemento necesario para especificar el origen del certificado que se va a utilizar con una autenticación EAP-TLS.</span><span class="sxs-lookup"><span data-stu-id="dca45-105">The **CredentialsSourceParameters** complex type defines the element required to specify the source of the certificate to be used with an EAP-TLS authentication.</span></span>

<span data-ttu-id="dca45-106">Existe una opción entre el elemento de [**tarjeta inteligente**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) o el elemento [**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) .</span><span class="sxs-lookup"><span data-stu-id="dca45-106">There is a choice between the [**SmartCard**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) element or [**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) element.</span></span>

``` syntax
<xs:complexType name="CredentialsSourceParameters">
    <xs:choice>
        <xs:element name="SmartCard"
            type="emptyString"
         />
        <xs:element name="CertificateStore"
            type="CertSelection"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="dca45-107">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="dca45-107">Child elements</span></span>



| <span data-ttu-id="dca45-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="dca45-108">Element</span></span>                                                                                                             | <span data-ttu-id="dca45-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="dca45-109">Type</span></span>                                                                                  | <span data-ttu-id="dca45-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="dca45-110">Description</span></span>                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dca45-111">**CertificateStore**</span><span class="sxs-lookup"><span data-stu-id="dca45-111">**CertificateStore**</span></span>](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) | [<span data-ttu-id="dca45-112">**CertSelection**</span><span class="sxs-lookup"><span data-stu-id="dca45-112">**CertSelection**</span></span>](eaptlsconnectionpropertiesv1schema-certselection-complextype.md) | <span data-ttu-id="dca45-113">Indica que EAP-TLS debe leer el certificado del almacén My del usuario o el equipo que se va a autenticar.</span><span class="sxs-lookup"><span data-stu-id="dca45-113">Indicates that EAP-TLS should read the certificate from the user's My Store, or the machine being authenticated.</span></span> <br/> |
| [<span data-ttu-id="dca45-114">**Tarjeta**</span><span class="sxs-lookup"><span data-stu-id="dca45-114">**SmartCard**</span></span>](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md)               | [<span data-ttu-id="dca45-115">**emptyString**</span><span class="sxs-lookup"><span data-stu-id="dca45-115">**emptyString**</span></span>](eaptlsconnectionpropertiesv1schema-emptystring-simpletype.md)      | <span data-ttu-id="dca45-116">Indica que EAP-TLS debe leer el certificado de la tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="dca45-116">Indicates that EAP-TLS should read the certificate from the Smart Card.</span></span> <br/>                                          |



## <a name="remarks"></a><span data-ttu-id="dca45-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dca45-117">Remarks</span></span>

<span data-ttu-id="dca45-118">Los elementos [**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) y [**SmartCard**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) no se pueden usar simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="dca45-118">The [**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) and [**SmartCard**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) elements cannot both be used simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="dca45-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dca45-119">Requirements</span></span>



| <span data-ttu-id="dca45-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="dca45-120">Requirement</span></span> | <span data-ttu-id="dca45-121">Value</span><span class="sxs-lookup"><span data-stu-id="dca45-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="dca45-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dca45-122">Minimum supported client</span></span><br/> | <span data-ttu-id="dca45-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="dca45-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="dca45-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dca45-124">Minimum supported server</span></span><br/> | <span data-ttu-id="dca45-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="dca45-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dca45-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="dca45-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dca45-127">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="dca45-127">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="dca45-128">Esquema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="dca45-128">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="dca45-129">Tipos complejos de esquema de eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="dca45-129">eaptlsconnectionpropertiesv1 Schema Complex Types</span></span>](eaptlsconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 





