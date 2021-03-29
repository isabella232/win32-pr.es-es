---
description: El proveedor base crea claves simétricas de 40 bits creadas con once bytes de sal de valor cero, once bytes de un valor Salt distinto de cero si \_ \_ se especifica CRYPT Create Salt, o ningún valor Salt.
ms.assetid: f1af0af7-c64e-435a-aef0-7c4ed7bd1199
title: Funcionalidad de valores Salt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd8e3049c431cf909c1008acac26925cd1fa9e6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360468"
---
# <a name="salt-value-functionality"></a><span data-ttu-id="7e226-103">Funcionalidad de valores Salt</span><span class="sxs-lookup"><span data-stu-id="7e226-103">Salt Value Functionality</span></span>

<span data-ttu-id="7e226-104">El proveedor base crea [*claves simétricas*](../secgloss/s-gly.md) de 40 bits creadas con once bytes de [*sal*](../secgloss/s-gly.md)de valor cero, once bytes de un valor Salt distinto de cero si \_ \_ se especifica CRYPT Create Salt, o ningún valor Salt.</span><span class="sxs-lookup"><span data-stu-id="7e226-104">The Base Provider creates 40-bit [*symmetric keys*](../secgloss/s-gly.md) created with eleven bytes of zero-value [*salt*](../secgloss/s-gly.md), eleven bytes of nonzero salt if CRYPT\_CREATE\_SALT is specified, or no salt value.</span></span> <span data-ttu-id="7e226-105">Sin embargo, una clave simétrica de 40 bits con sal de valor cero no es equivalente a una clave simétrica de 40 bits sin sal.</span><span class="sxs-lookup"><span data-stu-id="7e226-105">A 40-bit symmetric key with zero-value salt, however, is not equivalent to a 40-bit symmetric key without salt.</span></span> <span data-ttu-id="7e226-106">Para la interoperabilidad, las claves se deben crear sin sal.</span><span class="sxs-lookup"><span data-stu-id="7e226-106">For interoperability, keys must be created without salt.</span></span> <span data-ttu-id="7e226-107">Este problema es el resultado de una condición predeterminada que solo se produce con claves de exactamente 40 bits.</span><span class="sxs-lookup"><span data-stu-id="7e226-107">This problem results from a default condition that occurs only with keys of exactly 40 bits.</span></span> <span data-ttu-id="7e226-108">El resto de las [*longitudes de clave*](../secgloss/k-gly.md) no tienen un valor Salt asignado de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="7e226-108">All other [*key lengths*](../secgloss/k-gly.md) do not have salt allocated by default.</span></span>

<span data-ttu-id="7e226-109">Tanto los proveedores de base como el proveedor extendido pueden utilizar la \_ marca CRYPT not \_ sal para especificar que no se asigna ningún valor Salt para una clave simétrica de 40 bits.</span><span class="sxs-lookup"><span data-stu-id="7e226-109">Both the Base Providers and the Extended Provider can use the CRYPT\_NO\_SALT flag to specify that no salt value is allocated for a 40-bit symmetric key.</span></span> <span data-ttu-id="7e226-110">Las funciones que aceptan esta marca son [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey), [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey)y [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).</span><span class="sxs-lookup"><span data-stu-id="7e226-110">The functions that accept this flag are [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey), [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey), and [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).</span></span> <span data-ttu-id="7e226-111">De forma predeterminada, estas funciones proporcionan compatibilidad con versiones anteriores para el caso de clave simétrica de 40 bits; para ello, se sigue usando el valor de sal de valor cero de once bytes.</span><span class="sxs-lookup"><span data-stu-id="7e226-111">By default, these functions provide backward compatibility for the 40-bit symmetric key case by continuing the use of the eleven-byte-long zero-value salt.</span></span>

 

 
