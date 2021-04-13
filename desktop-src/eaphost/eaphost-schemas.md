---
title: EAPHost y esquema heredado
description: Describe el esquema de EAPHost y el esquema heredado para crear el XML de configuración y el XML de credenciales.
ms.assetid: d4572866-7e2b-4e7c-afe1-66394b549bc4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dbe40f447618a9ca0da89875521349101c1191f
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "104420033"
---
# <a name="eaphost-and-legacy-schema"></a><span data-ttu-id="1f1a6-103">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="1f1a6-103">EAPHost and Legacy Schema</span></span>

<span data-ttu-id="1f1a6-104">En este tema se describe el esquema de EAPHost y el esquema heredado para crear XML de configuración y el XML de credenciales.</span><span class="sxs-lookup"><span data-stu-id="1f1a6-104">This topic describes the EAPHost schema and legacy schema for creating configuration XML and credential XML.</span></span>

## <a name="about-eaphost-and-legacy-schema"></a><span data-ttu-id="1f1a6-105">Acerca de EAPHost y el esquema heredado</span><span class="sxs-lookup"><span data-stu-id="1f1a6-105">About EAPHost and Legacy Schema</span></span>

<span data-ttu-id="1f1a6-106">La creación de XML de configuración comienza con el esquema [eaphostconfig](eaphostconfigschema-schema.md) ; la creación de XML de credenciales comienza con el esquema [eaphostusercredentials](eaphostusercredentialsschema-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="1f1a6-106">Creating configuration XML commences with the [eaphostconfig](eaphostconfigschema-schema.md) schema; creating credential XML commences with the [eaphostusercredentials](eaphostusercredentialsschema-schema.md) schema.</span></span>

<span data-ttu-id="1f1a6-107">Algunos de los esquemas nativos y heredados contienen elementos de esquema comunes.</span><span class="sxs-lookup"><span data-stu-id="1f1a6-107">Several of the native and legacy schema contain common schema elements.</span></span> <span data-ttu-id="1f1a6-108">Los elementos comunes que se usan en la configuración de métodos y las credenciales de método se abstraen en un solo archivo de esquema, que se conoce como "esquema común".</span><span class="sxs-lookup"><span data-stu-id="1f1a6-108">Common elements used in method configuration and method credentials are abstracted into a single schema file, referred to as the "common schema".</span></span>

<span data-ttu-id="1f1a6-109">Los términos "configuración de método" y "propiedades de conexión" se usan indistintamente.</span><span class="sxs-lookup"><span data-stu-id="1f1a6-109">The terms "method configuration" and "connection properties" are used interchangeably.</span></span> <span data-ttu-id="1f1a6-110">Del mismo modo, los términos "credenciales de método" y "propiedades de usuario" también se usan indistintamente.</span><span class="sxs-lookup"><span data-stu-id="1f1a6-110">Likewise, the terms "method credentials" and "user properties" are also used interchangeably.</span></span>

## <a name="eaphost-schema"></a><span data-ttu-id="1f1a6-111">Esquema de EAPHost</span><span class="sxs-lookup"><span data-stu-id="1f1a6-111">EAPHost Schema</span></span>



| <span data-ttu-id="1f1a6-112">Schema</span><span class="sxs-lookup"><span data-stu-id="1f1a6-112">Schema</span></span>                                                                        | <span data-ttu-id="1f1a6-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="1f1a6-113">Description</span></span>                                        |
|-------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="1f1a6-114">baseeapmethodconfig</span><span class="sxs-lookup"><span data-stu-id="1f1a6-114">baseeapmethodconfig</span></span>](baseeapmethodconfigschema-schema.md)                   | <span data-ttu-id="1f1a6-115">Contiene elementos de esquema de configuración comunes.</span><span class="sxs-lookup"><span data-stu-id="1f1a6-115">Contains common configuration schema elements.</span></span>     |
| [<span data-ttu-id="1f1a6-116">baseeapmethodusercredentials</span><span class="sxs-lookup"><span data-stu-id="1f1a6-116">baseeapmethodusercredentials</span></span>](baseeapmethodusercredentialsschema-schema.md) | <span data-ttu-id="1f1a6-117">Contiene elementos comunes del esquema de credenciales.</span><span class="sxs-lookup"><span data-stu-id="1f1a6-117">Contains common credential schema elements.</span></span>        |
| [<span data-ttu-id="1f1a6-118">eapcommon</span><span class="sxs-lookup"><span data-stu-id="1f1a6-118">eapcommon</span></span>](eapcommonschema-schema.md)                                       | <span data-ttu-id="1f1a6-119">Contiene la definición del elemento **EapMethodType** .</span><span class="sxs-lookup"><span data-stu-id="1f1a6-119">Contains the **EapMethodType** element definition.</span></span> |
| [<span data-ttu-id="1f1a6-120">eaphostconfig</span><span class="sxs-lookup"><span data-stu-id="1f1a6-120">eaphostconfig</span></span>](eaphostconfigschema-schema.md)                               | <span data-ttu-id="1f1a6-121">Contiene el esquema de configuración de EAPHost.</span><span class="sxs-lookup"><span data-stu-id="1f1a6-121">Contains EAPHost configuration schema.</span></span>             |
| [<span data-ttu-id="1f1a6-122">eaphostusercredentials</span><span class="sxs-lookup"><span data-stu-id="1f1a6-122">eaphostusercredentials</span></span>](eaphostusercredentialsschema-schema.md)             | <span data-ttu-id="1f1a6-123">Contiene el esquema de credenciales de EAPHost.</span><span class="sxs-lookup"><span data-stu-id="1f1a6-123">Contains EAPHost credential schema.</span></span>                |



 

## <a name="legacy-schema"></a><span data-ttu-id="1f1a6-124">Esquema heredado</span><span class="sxs-lookup"><span data-stu-id="1f1a6-124">Legacy Schema</span></span>



| <span data-ttu-id="1f1a6-125">Schema</span><span class="sxs-lookup"><span data-stu-id="1f1a6-125">Schema</span></span>                                                                            | <span data-ttu-id="1f1a6-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="1f1a6-126">Description</span></span>                                                                                  |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1f1a6-127">baseeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="1f1a6-127">baseeapconnectionpropertiesv1</span></span>](baseeapconnectionpropertiesv1schema-schema.md)   | <span data-ttu-id="1f1a6-128">Contiene elementos de esquema de configuración comunes.</span><span class="sxs-lookup"><span data-stu-id="1f1a6-128">Contains common configuration schema elements.</span></span>                                               |
| [<span data-ttu-id="1f1a6-129">baseeapuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="1f1a6-129">baseeapuserpropertiesv1</span></span>](baseeapuserpropertiesv1schema-schema.md)               | <span data-ttu-id="1f1a6-130">Contiene elementos comunes del esquema de credenciales.</span><span class="sxs-lookup"><span data-stu-id="1f1a6-130">Contains common credential schema elements.</span></span>                                                  |
| [<span data-ttu-id="1f1a6-131">eapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="1f1a6-131">eapconnectionpropertiesv1</span></span>](eapconnectionpropertiesv1schema-schema.md)           | <span data-ttu-id="1f1a6-132">Contiene elementos de esquema de configuración comunes.</span><span class="sxs-lookup"><span data-stu-id="1f1a6-132">Contains common configuration schema elements.</span></span>                                               |
| [<span data-ttu-id="1f1a6-133">eapuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="1f1a6-133">eapuserpropertiesv1</span></span>](eapuserpropertiesv1schema-schema.md)                       | <span data-ttu-id="1f1a6-134">Contiene elementos comunes del esquema de credenciales.</span><span class="sxs-lookup"><span data-stu-id="1f1a6-134">Contains common credential schema elements.</span></span>                                                  |
| [<span data-ttu-id="1f1a6-135">eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="1f1a6-135">eaptlsconnectionpropertiesv1</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)     | <span data-ttu-id="1f1a6-136">Se usa con EAP-TLS para describir los datos de configuración de autenticación.</span><span class="sxs-lookup"><span data-stu-id="1f1a6-136">Is used with EAP-TLS to describe authentication configuration data.</span></span>                          |
| [<span data-ttu-id="1f1a6-137">eaptlsconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="1f1a6-137">eaptlsconnectionpropertiesv2</span></span>](eaptlsconnectionpropertiesv2schema-schema.md)     | <span data-ttu-id="1f1a6-138">Se usa con EAP-TLS para describir los datos de configuración de autenticación a partir de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1f1a6-138">Is used with EAP-TLS to describe authentication configuration data beginning with Windows 7.</span></span> |
| [<span data-ttu-id="1f1a6-139">eaptlsuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="1f1a6-139">eaptlsuserpropertiesv1</span></span>](eaptlsuserpropertiesv1schema-schema.md)                 | <span data-ttu-id="1f1a6-140">Se usa con EAP-TLS para describir las credenciales de autenticación y las opciones de credenciales.</span><span class="sxs-lookup"><span data-stu-id="1f1a6-140">Is used with EAP-TLS to describe authentication credentials and credential options.</span></span>          |
| [<span data-ttu-id="1f1a6-141">mschapv2connectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="1f1a6-141">mschapv2connectionpropertiesv1</span></span>](mschapv2connectionpropertiesv1schema-schema.md) | <span data-ttu-id="1f1a6-142">Se utiliza con MS-CHAPv2 para describir los datos de configuración de autenticación.</span><span class="sxs-lookup"><span data-stu-id="1f1a6-142">Is used with MS-CHAPv2 to describe authentication configuration data.</span></span>                        |
| [<span data-ttu-id="1f1a6-143">mschapv2userpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="1f1a6-143">mschapv2userpropertiesv1</span></span>](mschapv2userpropertiesv1schema-schema.md)             | <span data-ttu-id="1f1a6-144">Se usa con MS-CHAPv2 para describir las credenciales de autenticación y las opciones de credenciales.</span><span class="sxs-lookup"><span data-stu-id="1f1a6-144">Is used with MS-CHAPv2 to describe authentication credentials and credential options.</span></span>        |
| [<span data-ttu-id="1f1a6-145">mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="1f1a6-145">mspeapconnectionpropertiesv1</span></span>](mspeapconnectionpropertiesv1schema-schema.md)     | <span data-ttu-id="1f1a6-146">Se usa con PEAPv0 para describir los datos de configuración de autenticación.</span><span class="sxs-lookup"><span data-stu-id="1f1a6-146">Is used with PEAPv0 to describe authentication configuration data.</span></span>                           |
| [<span data-ttu-id="1f1a6-147">mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="1f1a6-147">mspeapconnectionpropertiesv2</span></span>](mspeapconnectionpropertiesv2schema-schema.md)     | <span data-ttu-id="1f1a6-148">Se usa con PEAPv0 para describir los datos de configuración de autenticación a partir de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1f1a6-148">Is used with PEAPv0 to describe authentication configuration data beginning with Windows 7.</span></span>  |
| [<span data-ttu-id="1f1a6-149">mspeapuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="1f1a6-149">mspeapuserpropertiesv1</span></span>](mspeapuserpropertiesv1schema-schema.md)                 | <span data-ttu-id="1f1a6-150">Se usa con PEAPv0 para describir las credenciales de autenticación y las opciones de credenciales.</span><span class="sxs-lookup"><span data-stu-id="1f1a6-150">Is used with PEAPv0 to describe authentication credentials and credential options.</span></span>           |



 

## <a name="related-topics"></a><span data-ttu-id="1f1a6-151">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1f1a6-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f1a6-152">Revisión de los ejemplos de los esquemas de EAPHost y heredado</span><span class="sxs-lookup"><span data-stu-id="1f1a6-152">Reviewing EAPHost and Legacy Schema Samples</span></span>](eaphost-schemas.md)
</dt> </dl>

 

 




