---
description: En el caso de las constantes de datos de marca de bits extensible, un proveedor de proveedor de servicios puede definir nuevos valores para los bits especificados.
ms.assetid: bf3ca2b0-a9fb-4e63-87de-6d5cbe5cd746
title: Constantes de datos de Bit-Flag
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 238627505bf414ed0ab94ff2f5c35197705c91d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687252"
---
# <a name="bit-flag-data-constants"></a><span data-ttu-id="b1e2c-103">Constantes de datos de Bit-Flag</span><span class="sxs-lookup"><span data-stu-id="b1e2c-103">Bit-Flag Data Constants</span></span>

<span data-ttu-id="b1e2c-104">En el caso de las constantes de datos de marca de bits extensible, un proveedor de proveedor de servicios puede definir nuevos valores para los bits especificados.</span><span class="sxs-lookup"><span data-stu-id="b1e2c-104">For extensible bit-flag data constants, a service-provider vendor can define new values for specified bits.</span></span> <span data-ttu-id="b1e2c-105">Dado que la mayoría de las constantes de marcador de bits son **DWORD** s, un número específico de los bits inferiores normalmente se reserva para las extensiones comunes, mientras que los bits superiores restantes están disponibles para las extensiones específicas del proveedor.</span><span class="sxs-lookup"><span data-stu-id="b1e2c-105">Because most bit-flag constants are **DWORD** s, a specific number of the lower bits are usually reserved for common extensions, while the remaining upper bits are available for vendor-specific extensions.</span></span> <span data-ttu-id="b1e2c-106">Las marcas de bits comunes se asignan a partir de cero bits hacia arriba y las extensiones específicas del proveedor deben asignarse desde el bit 31 hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="b1e2c-106">Common bit flags are assigned from bit zero up, and vendor-specific extensions should be assigned from bit 31 down.</span></span> <span data-ttu-id="b1e2c-107">Este esquema proporciona la máxima flexibilidad a la hora de asignar posiciones de bits a extensiones comunes, en lugar de extensiones específicas del proveedor.</span><span class="sxs-lookup"><span data-stu-id="b1e2c-107">This scheme provides maximum flexibility in assigning bit positions to common extensions, as opposed to vendor-specific extensions.</span></span> <span data-ttu-id="b1e2c-108">Se espera que un proveedor defina nuevos valores que son extensiones naturales de las marcas de bits definidas por la API.</span><span class="sxs-lookup"><span data-stu-id="b1e2c-108">A vendor is expected to define new values that are natural extensions of the bit flags defined by the API.</span></span>

<span data-ttu-id="b1e2c-109">Las estructuras de datos extensibles tienen un campo de tamaño variable que se reserva para uso específico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b1e2c-109">Extensible data structures have a variably sized field that is reserved for device-specific use.</span></span> <span data-ttu-id="b1e2c-110">Dado que el campo tiene un tamaño de variable, el proveedor de servicios decide la cantidad de información e interpretación del campo.</span><span class="sxs-lookup"><span data-stu-id="b1e2c-110">Because the field is variably sized, the service provider decides the field's amount of information and interpretation.</span></span> <span data-ttu-id="b1e2c-111">Se espera que un proveedor que define un campo específico del dispositivo realice estas extensiones naturales de la estructura de datos original definida por la API.</span><span class="sxs-lookup"><span data-stu-id="b1e2c-111">A vendor that defines a device-specific field is expected to make these natural extensions of the original data structure defined by the API.</span></span>

 

 



