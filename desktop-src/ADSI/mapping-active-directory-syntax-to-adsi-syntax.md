---
title: Asignar Active Directory sintaxis a la sintaxis ADSI
description: En la tabla siguiente se asignan las sintaxis de Active Directory a sus correspondientes sintaxis de ADSI.
ms.assetid: ffb40eff-e137-4d6a-81e7-24d2cbbdbfbf
ms.tgt_platform: multiple
keywords:
- atributos ADSI, asignar sintaxis Active Directory a la sintaxis ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6ba332a39a5d2452925f1a8f1cc8c8ca766ca10
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656165"
---
# <a name="mapping-active-directory-syntax-to-adsi-syntax"></a><span data-ttu-id="66ac8-104">Asignar Active Directory sintaxis a la sintaxis ADSI</span><span class="sxs-lookup"><span data-stu-id="66ac8-104">Mapping Active Directory Syntax to ADSI Syntax</span></span>

<span data-ttu-id="66ac8-105">En la tabla siguiente se asignan las sintaxis de Active Directory a sus correspondientes sintaxis de ADSI.</span><span class="sxs-lookup"><span data-stu-id="66ac8-105">The following table maps the Active Directory syntaxes to their corresponding ADSI syntaxes.</span></span>



| <span data-ttu-id="66ac8-106">IDENTIFICADOR de sintaxis de atributo</span><span class="sxs-lookup"><span data-stu-id="66ac8-106">Attribute syntax ID</span></span> | <span data-ttu-id="66ac8-107">Active Directory tipo de sintaxis</span><span class="sxs-lookup"><span data-stu-id="66ac8-107">Active Directory syntax type</span></span>             | <span data-ttu-id="66ac8-108">Tipo de sintaxis ADSI equivalente</span><span class="sxs-lookup"><span data-stu-id="66ac8-108">Equivalent ADSI syntax type</span></span>                                         |
|---------------------|------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="66ac8-109">2.5.5.1</span><span class="sxs-lookup"><span data-stu-id="66ac8-109">2.5.5.1</span></span><br/>  | <span data-ttu-id="66ac8-110">Cadena DN</span><span class="sxs-lookup"><span data-stu-id="66ac8-110">DN String</span></span><br/>                     | <span data-ttu-id="66ac8-111">Cadena DN</span><span class="sxs-lookup"><span data-stu-id="66ac8-111">DN String</span></span><br/>                                                |
| <span data-ttu-id="66ac8-112">2.5.5.2</span><span class="sxs-lookup"><span data-stu-id="66ac8-112">2.5.5.2</span></span><br/>  | <span data-ttu-id="66ac8-113">Identificador de objeto</span><span class="sxs-lookup"><span data-stu-id="66ac8-113">Object ID</span></span><br/>                     | <span data-ttu-id="66ac8-114">Cadena CaseIgnore</span><span class="sxs-lookup"><span data-stu-id="66ac8-114">CaseIgnore String</span></span><br/>                                        |
| <span data-ttu-id="66ac8-115">2.5.5.3</span><span class="sxs-lookup"><span data-stu-id="66ac8-115">2.5.5.3</span></span><br/>  | <span data-ttu-id="66ac8-116">Cadena que distingue mayúsculas de minúsculas</span><span class="sxs-lookup"><span data-stu-id="66ac8-116">Case Sensitive String</span></span><br/>         | <span data-ttu-id="66ac8-117">Cadena CaseExact</span><span class="sxs-lookup"><span data-stu-id="66ac8-117">CaseExact String</span></span><br/>                                         |
| <span data-ttu-id="66ac8-118">2.5.5.4</span><span class="sxs-lookup"><span data-stu-id="66ac8-118">2.5.5.4</span></span><br/>  | <span data-ttu-id="66ac8-119">Caso de cadena omitida</span><span class="sxs-lookup"><span data-stu-id="66ac8-119">Case Ignored String</span></span><br/>           | <span data-ttu-id="66ac8-120">Cadena CaseIgnore</span><span class="sxs-lookup"><span data-stu-id="66ac8-120">CaseIgnore String</span></span><br/>                                        |
| <span data-ttu-id="66ac8-121">2.5.5.5</span><span class="sxs-lookup"><span data-stu-id="66ac8-121">2.5.5.5</span></span><br/>  | <span data-ttu-id="66ac8-122">Cadena de caso de impresión</span><span class="sxs-lookup"><span data-stu-id="66ac8-122">Print Case String</span></span><br/>             | <span data-ttu-id="66ac8-123">Cadena imprimible</span><span class="sxs-lookup"><span data-stu-id="66ac8-123">Printable String</span></span><br/>                                         |
| <span data-ttu-id="66ac8-124">2.5.5.6</span><span class="sxs-lookup"><span data-stu-id="66ac8-124">2.5.5.6</span></span><br/>  | <span data-ttu-id="66ac8-125">Cadena numérica</span><span class="sxs-lookup"><span data-stu-id="66ac8-125">Numeric String</span></span><br/>                | <span data-ttu-id="66ac8-126">Cadena numérica</span><span class="sxs-lookup"><span data-stu-id="66ac8-126">Numeric String</span></span><br/>                                           |
| <span data-ttu-id="66ac8-127">2.5.5.7</span><span class="sxs-lookup"><span data-stu-id="66ac8-127">2.5.5.7</span></span><br/>  | <span data-ttu-id="66ac8-128">**O bien** Nombre DNWithOctetString</span><span class="sxs-lookup"><span data-stu-id="66ac8-128">**OR** Name DNWithOctetString</span></span><br/> | <span data-ttu-id="66ac8-129">No compatible</span><span class="sxs-lookup"><span data-stu-id="66ac8-129">Not Supported</span></span><br/>                                            |
| <span data-ttu-id="66ac8-130">2.5.5.8</span><span class="sxs-lookup"><span data-stu-id="66ac8-130">2.5.5.8</span></span><br/>  | <span data-ttu-id="66ac8-131">Boolean</span><span class="sxs-lookup"><span data-stu-id="66ac8-131">Boolean</span></span><br/>                       | <span data-ttu-id="66ac8-132">Boolean</span><span class="sxs-lookup"><span data-stu-id="66ac8-132">Boolean</span></span><br/>                                                  |
| <span data-ttu-id="66ac8-133">2.5.5.9</span><span class="sxs-lookup"><span data-stu-id="66ac8-133">2.5.5.9</span></span><br/>  | <span data-ttu-id="66ac8-134">Entero</span><span class="sxs-lookup"><span data-stu-id="66ac8-134">Integer</span></span><br/>                       | <span data-ttu-id="66ac8-135">Entero</span><span class="sxs-lookup"><span data-stu-id="66ac8-135">Integer</span></span><br/>                                                  |
| <span data-ttu-id="66ac8-136">2.5.5.10</span><span class="sxs-lookup"><span data-stu-id="66ac8-136">2.5.5.10</span></span><br/> | <span data-ttu-id="66ac8-137">Cadena de octeto</span><span class="sxs-lookup"><span data-stu-id="66ac8-137">Octet String</span></span><br/>                  | <span data-ttu-id="66ac8-138">Cadena de octeto</span><span class="sxs-lookup"><span data-stu-id="66ac8-138">Octet String</span></span><br/>                                             |
| <span data-ttu-id="66ac8-139">2.5.5.11</span><span class="sxs-lookup"><span data-stu-id="66ac8-139">2.5.5.11</span></span><br/> | <span data-ttu-id="66ac8-140">Hora</span><span class="sxs-lookup"><span data-stu-id="66ac8-140">Time</span></span><br/>                          | <span data-ttu-id="66ac8-141">Hora UTC</span><span class="sxs-lookup"><span data-stu-id="66ac8-141">UTC Time</span></span><br/>                                                 |
| <span data-ttu-id="66ac8-142">2.5.5.12</span><span class="sxs-lookup"><span data-stu-id="66ac8-142">2.5.5.12</span></span><br/> | <span data-ttu-id="66ac8-143">Unicode</span><span class="sxs-lookup"><span data-stu-id="66ac8-143">Unicode</span></span><br/>                       | <span data-ttu-id="66ac8-144">Distinción de mayúsculas y minúsculas</span><span class="sxs-lookup"><span data-stu-id="66ac8-144">Case Ignore String</span></span><br/>                                       |
| <span data-ttu-id="66ac8-145">2.5.5.13</span><span class="sxs-lookup"><span data-stu-id="66ac8-145">2.5.5.13</span></span><br/> | <span data-ttu-id="66ac8-146">Dirección</span><span class="sxs-lookup"><span data-stu-id="66ac8-146">Address</span></span><br/>                       | <span data-ttu-id="66ac8-147">No compatible</span><span class="sxs-lookup"><span data-stu-id="66ac8-147">Not Supported</span></span><br/>                                            |
| <span data-ttu-id="66ac8-148">2.5.5.14</span><span class="sxs-lookup"><span data-stu-id="66ac8-148">2.5.5.14</span></span><br/> | <span data-ttu-id="66ac8-149">Distname-Address</span><span class="sxs-lookup"><span data-stu-id="66ac8-149">Distname-Address</span></span><br/>              |                                                                     |
| <span data-ttu-id="66ac8-150">2.5.5.15</span><span class="sxs-lookup"><span data-stu-id="66ac8-150">2.5.5.15</span></span><br/> | <span data-ttu-id="66ac8-151">Descriptor de seguridad de NT</span><span class="sxs-lookup"><span data-stu-id="66ac8-151">NT Security Descriptor</span></span><br/>        | [<span data-ttu-id="66ac8-152">**IADsSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="66ac8-152">**IADsSecurityDescriptor**</span></span>](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)<br/> |
| <span data-ttu-id="66ac8-153">2.5.5.16</span><span class="sxs-lookup"><span data-stu-id="66ac8-153">2.5.5.16</span></span><br/> | <span data-ttu-id="66ac8-154">Entero grande</span><span class="sxs-lookup"><span data-stu-id="66ac8-154">Large Integer</span></span><br/>                 | [<span data-ttu-id="66ac8-155">**IADsLargeInteger**</span><span class="sxs-lookup"><span data-stu-id="66ac8-155">**IADsLargeInteger**</span></span>](/windows/desktop/api/Iads/nn-iads-iadslargeinteger)<br/>             |
| <span data-ttu-id="66ac8-156">2.5.5.17</span><span class="sxs-lookup"><span data-stu-id="66ac8-156">2.5.5.17</span></span><br/> | <span data-ttu-id="66ac8-157">SID</span><span class="sxs-lookup"><span data-stu-id="66ac8-157">SID</span></span><br/>                           | <span data-ttu-id="66ac8-158">Cadena de octeto</span><span class="sxs-lookup"><span data-stu-id="66ac8-158">Octet String</span></span><br/>                                             |



 

 

 





