---
description: La extensibilidad se consigue proporcionando el uso de nuevos identificadores de objeto (OID), nuevos tipos de codificación y nuevos archivos dll.
ms.assetid: 95e992fe-af30-4b4e-b20d-cfe5318d0a38
title: Información general sobre OID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cc371d18bd144ac68c7bc95d7b3ef71140b2e1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911585"
---
# <a name="oid-overview"></a><span data-ttu-id="02475-103">Información general sobre OID</span><span class="sxs-lookup"><span data-stu-id="02475-103">OID Overview</span></span>

<span data-ttu-id="02475-104">La extensibilidad se consigue proporcionando el uso de nuevos [*identificadores de objeto*](../secgloss/o-gly.md) (OID), nuevos tipos de codificación y nuevos archivos dll.</span><span class="sxs-lookup"><span data-stu-id="02475-104">Extensibility is achieved by providing for the use of new [*object identifiers*](../secgloss/o-gly.md) (OIDs), new encoding types, and new DLLs.</span></span>

<span data-ttu-id="02475-105">Los OID de CryptoAPI pueden adoptar cualquiera de las siguientes formas:</span><span class="sxs-lookup"><span data-stu-id="02475-105">CryptoAPI OIDs can take any of the following forms:</span></span>

-   <span data-ttu-id="02475-106">Una cadena numérica como "1.2.3.500.88"</span><span class="sxs-lookup"><span data-stu-id="02475-106">A numeric string such as "1.2.3.500.88"</span></span>
-   <span data-ttu-id="02475-107">Una cadena alfanumérica como *myFunction*</span><span class="sxs-lookup"><span data-stu-id="02475-107">An alphanumeric string such as *MyFunction*</span></span>
-   <span data-ttu-id="02475-108">Constante con un valor menor o igual que 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="02475-108">A constant with a value that is less than or equal to 0xFFFF.</span></span> <span data-ttu-id="02475-109">Estas constantes se suelen asociar a un nombre mediante el uso de una instrucción **\# define** en un archivo de encabezado.</span><span class="sxs-lookup"><span data-stu-id="02475-109">These constants are often associated with a name through the use of a **\#define** statement in a header file.</span></span>

<span data-ttu-id="02475-110">Las funciones extensibles aceptan OID y los argumentos de tipo de codificación.</span><span class="sxs-lookup"><span data-stu-id="02475-110">Extensible functions accept OID and encoding type arguments.</span></span> <span data-ttu-id="02475-111">Estas funciones buscan el registro del sistema para encontrar un archivo DLL asociado con el OID y los argumentos de tipo de codificación pasados a la función.</span><span class="sxs-lookup"><span data-stu-id="02475-111">These functions search the system registry to find a DLL associated with the OID and encoding type arguments passed to the function.</span></span> <span data-ttu-id="02475-112">Si se encuentra un archivo DLL para la combinación de tipo de codificación OID, el archivo DLL se carga y se llama a su función.</span><span class="sxs-lookup"><span data-stu-id="02475-112">If a DLL for the OID, encoding type combination is found, the DLL is loaded and its function is called.</span></span> <span data-ttu-id="02475-113">En la siguiente ilustración se muestra este flujo para la función [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) :</span><span class="sxs-lookup"><span data-stu-id="02475-113">The following illustration shows this flow for the [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) function:</span></span>

![flujo de OID](images/oidflow.png)

<span data-ttu-id="02475-115">Esto permite que la funcionalidad de CryptoAPI se extienda a medida que sea necesario.</span><span class="sxs-lookup"><span data-stu-id="02475-115">This allows the functionality of the CryptoAPI to be extended as the need arises.</span></span> <span data-ttu-id="02475-116">El uso de esta metodología supone una carga para el desarrollador de la nueva funcionalidad para escribir todo el código necesario para esa funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="02475-116">Use of this methodology places a burden on the developer of the new functionality to write all the necessary code for that functionality.</span></span> <span data-ttu-id="02475-117">Para codificar una nueva estructura de datos, por ejemplo, la función de la DLL debe realizar todo el proceso de codificación.</span><span class="sxs-lookup"><span data-stu-id="02475-117">To encode some new data structure, for example, the function in the DLL must perform the entire encoding process.</span></span>

 

 
