---
title: Configuración de límites de TTL
description: Un cliente puede solicitar un valor de TTL para una entrada comprendida entre 1 y 31557600 (es decir, de 1 segundo a 1 año).
ms.assetid: 4009702c-7992-4e20-9d37-384f8137ba8f
ms.tgt_platform: multiple
keywords:
- Configuración de límites de TTL de AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2cb3617bd59667f0284c4e383da54752adfbe25
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772732"
---
# <a name="configuration-of-ttl-limits"></a><span data-ttu-id="e755a-104">Configuración de límites de TTL</span><span class="sxs-lookup"><span data-stu-id="e755a-104">Configuration of TTL Limits</span></span>

<span data-ttu-id="e755a-105">Un cliente puede solicitar un valor de TTL para una entrada comprendida entre 1 y 31557600 (es decir, de 1 segundo a 1 año).</span><span class="sxs-lookup"><span data-stu-id="e755a-105">A client can request a TTL value for an entry ranging between 1 and 31557600 (that is, from 1 second to 1 year).</span></span> <span data-ttu-id="e755a-106">Los valores del atributo **rangeLower** y **rangeUpper** aplicarán este intervalo de valores de atributo en la definición de **attributeSchema** para el atributo **entryTTL** .</span><span class="sxs-lookup"><span data-stu-id="e755a-106">This attribute value range will be enforced by the **rangeLower** and **rangeUpper** attribute values in the **attributeSchema** definition for the **entryTTL** attribute.</span></span> <span data-ttu-id="e755a-107">Según RFC 2589, no es necesario que los servidores de directorio acepten este valor y que devuelvan un valor de TTL diferente al cliente.</span><span class="sxs-lookup"><span data-stu-id="e755a-107">As per RFC 2589, directory servers are not required to accept this value and might return a different TTL value to the client.</span></span> <span data-ttu-id="e755a-108">Los clientes deben poder usar este valor dictado por el servidor como período de actualización del cliente (CRP), que regirá la frecuencia con la que el cliente necesitará realizar la operación de actualización en la entrada dinámica.</span><span class="sxs-lookup"><span data-stu-id="e755a-108">Clients must be able to use this server-dictated value as their client refresh period (CRP) which will govern how often the client will need to perform the refresh operation on the dynamic entry.</span></span>

<span data-ttu-id="e755a-109">Active Directory Domain Services proporcionar a los administradores la capacidad de configurar los valores predeterminados y mínimos de TTL para un bosque.</span><span class="sxs-lookup"><span data-stu-id="e755a-109">Active Directory Domain Services provide administrators with the ability to configure the default and minimum TTL values for a forest.</span></span> <span data-ttu-id="e755a-110">El valor TTL predeterminado es lo que se asignará a una entrada dinámica recién creada si no se especifica un TTL explícitamente.</span><span class="sxs-lookup"><span data-stu-id="e755a-110">The default TTL value is what will be assigned to a newly created dynamic entry if a TTL is not explicitly specified.</span></span> <span data-ttu-id="e755a-111">El TTL mínimo invalidará cualquier valor de TTL especificado por el cliente inferior al mínimo configurado.</span><span class="sxs-lookup"><span data-stu-id="e755a-111">The minimum TTL will override any client specified TTL value that is lower than the configured minimum.</span></span> <span data-ttu-id="e755a-112">No se debe proporcionar ningún valor TTL máximo configurable porque el valor del atributo **rangeUpper** del objeto **attributeSchema** impondrá un máximo.</span><span class="sxs-lookup"><span data-stu-id="e755a-112">No configurable maximum TTL value needs to be provided because a maximum will be imposed by the **rangeUpper** attribute value in the **attributeSchema** object.</span></span> <span data-ttu-id="e755a-113">Permitir a los administradores configurar estos valores les permitirá establecer valores de TTL que aplicarán un tráfico de poca actualización o, en el otro extremo, proporcionarán un directorio muy actualizado.</span><span class="sxs-lookup"><span data-stu-id="e755a-113">Allowing administrators to configure these values will enable them to set TTL values which will enforce a low refresh traffic or, at the other extreme, provide a highly up-to-date directory.</span></span>

<span data-ttu-id="e755a-114">Los valores predeterminados para los dos parámetros de TTL configurables serán los siguientes:</span><span class="sxs-lookup"><span data-stu-id="e755a-114">The default values for the two configurable TTL parameters will be as follows:</span></span>

-   <span data-ttu-id="e755a-115">Valor TTL predeterminado = 86400 segundos (1 día)</span><span class="sxs-lookup"><span data-stu-id="e755a-115">Default TTL value = 86400 seconds (1 day)</span></span>
-   <span data-ttu-id="e755a-116">Valor TTL mínimo = 900 segundos (15 minutos)</span><span class="sxs-lookup"><span data-stu-id="e755a-116">Minimum TTL value = 900 seconds (15 minutes)</span></span>

<span data-ttu-id="e755a-117">Los parámetros de TTL que se pueden configurar se almacenarán como entradas de AVA (aserción de valor de atributo) con el formato "<nombre-valor>=</span><span class="sxs-lookup"><span data-stu-id="e755a-117">The configurable TTL parameters will be stored as AVA (attribute value assertion) entries of the form "<value-name>=</span></span><value><span data-ttu-id="e755a-118">"en el atributo **MS-DS-Other-Settings** del objeto NTDS-Service proporcionado por el DN siguiente en la partición de configuración:</span><span class="sxs-lookup"><span data-stu-id="e755a-118">" in the attribute **ms-DS-Other-Settings** of the NTDS-Service object given by the following DN in the Configuration partition:</span></span>


```C++
CN=Directory Service,CN=Windows NT,CN=Services,CN=Configuration,DC=...
```



<span data-ttu-id="e755a-119">La sintaxis exacta de AVA, para los dos parámetros de TTL configurables, es la siguiente, donde NNNN se expresa en segundos:</span><span class="sxs-lookup"><span data-stu-id="e755a-119">The exact AVA syntax, for the two configurable TTL parameters, is as follows where NNNN is expressed in seconds:</span></span>


```C++
DynamicObjectDefaultTTLSeconds=NNNN
```




```C++
DynamicObjectMinTTLSeconds=NNNN
```



<span data-ttu-id="e755a-120">Los administradores pueden establecer estos valores a través de la utilidad de línea de comandos Ntdsutil.</span><span class="sxs-lookup"><span data-stu-id="e755a-120">These values can be set by an administrator through the command-line utility ntdsutil.</span></span>

 

 




