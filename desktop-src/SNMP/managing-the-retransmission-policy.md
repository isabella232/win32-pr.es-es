---
title: Administrar la Directiva de retransmisión
description: La aplicación WinSNMP puede solicitar que la implementación de Microsoft WinSNMP ejecute la Directiva de retransmisión de la aplicación. Cuando la implementación administra la retransmisión, usa el período de tiempo de espera y los valores de número de reintentos en su base de datos.
ms.assetid: 1f1a9589-3566-4d90-ac4d-7acf69f34676
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f2e47d983f8da62ccb8ffbe9c20b35c71bfbb70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076052"
---
# <a name="managing-the-retransmission-policy"></a><span data-ttu-id="59c34-104">Administrar la Directiva de retransmisión</span><span class="sxs-lookup"><span data-stu-id="59c34-104">Managing the Retransmission Policy</span></span>

<span data-ttu-id="59c34-105">La aplicación WinSNMP puede solicitar que la implementación de Microsoft WinSNMP ejecute la Directiva de retransmisión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="59c34-105">The WinSNMP application can request that the Microsoft WinSNMP implementation execute the application's retransmission policy.</span></span> <span data-ttu-id="59c34-106">Cuando la implementación administra la retransmisión, usa el período de tiempo de espera y los valores de número de reintentos en su base de datos.</span><span class="sxs-lookup"><span data-stu-id="59c34-106">When the implementation manages retransmission, it uses the time-out period and the retry count values in its database.</span></span>

<span data-ttu-id="59c34-107">La implementación de identifica el modo de retransmisión predeterminado en un valor devuelto de la función [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) durante la inicialización.</span><span class="sxs-lookup"><span data-stu-id="59c34-107">The implementation identifies the default retransmission mode in a return value from the [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) function during initialization.</span></span> <span data-ttu-id="59c34-108">El modo puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="59c34-108">The mode can be one of the following values.</span></span>



| <span data-ttu-id="59c34-109">Value</span><span class="sxs-lookup"><span data-stu-id="59c34-109">Value</span></span>        | <span data-ttu-id="59c34-110">Significado</span><span class="sxs-lookup"><span data-stu-id="59c34-110">Meaning</span></span>                                                                      |
|--------------|------------------------------------------------------------------------------|
| <span data-ttu-id="59c34-111">SNMPAPI \_</span><span class="sxs-lookup"><span data-stu-id="59c34-111">SNMPAPI\_ON</span></span>  | <span data-ttu-id="59c34-112">La implementación está ejecutando la Directiva de retransmisión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="59c34-112">The implementation is executing the application's retransmission policy.</span></span>     |
| <span data-ttu-id="59c34-113">SNMPAPI \_ desactivado</span><span class="sxs-lookup"><span data-stu-id="59c34-113">SNMPAPI\_OFF</span></span> | <span data-ttu-id="59c34-114">La implementación no está ejecutando la Directiva de retransmisión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="59c34-114">The implementation is not executing the application's retransmission policy.</span></span> |



 

<span data-ttu-id="59c34-115">Una aplicación WinSNMP puede recuperar en cualquier momento el modo de retransmisión actual en vigor para la implementación mediante una llamada a la función [**SnmpGetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretransmitmode) .</span><span class="sxs-lookup"><span data-stu-id="59c34-115">A WinSNMP application can retrieve at any time the current retransmission mode in effect for the implementation by calling the [**SnmpGetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretransmitmode) function.</span></span> <span data-ttu-id="59c34-116">La API WinSNMP proporciona otras [funciones de base de datos](winsnmp-functions.md) que simplifican la administración de la Directiva de retransmisión.</span><span class="sxs-lookup"><span data-stu-id="59c34-116">The WinSNMP API provides other [database functions](winsnmp-functions.md) that simplify management of the retransmission policy.</span></span>

<span data-ttu-id="59c34-117">En cualquier momento durante la ejecución del programa, la aplicación WinSNMP puede ajustar la ejecución de la Directiva llevando a cabo uno de los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="59c34-117">At any time during program execution, the WinSNMP application can adjust execution of the policy by performing one of the following steps:</span></span>

-   <span data-ttu-id="59c34-118">Solicite que la implementación inicie o detenga la ejecución de la Directiva de retransmisión mediante una llamada a la función [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) .</span><span class="sxs-lookup"><span data-stu-id="59c34-118">Request that the implementation start or stop executing the retransmission policy by calling the [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) function.</span></span> <span data-ttu-id="59c34-119">Para obtener más información, consulte [activación y desactivación de la retransmisión](turning-retransmission-on-and-off.md).</span><span class="sxs-lookup"><span data-stu-id="59c34-119">For more information, see [Turning Retransmission On and Off](turning-retransmission-on-and-off.md).</span></span>
-   <span data-ttu-id="59c34-120">Modifique el período de tiempo de espera y los valores de número de reintentos en la base de datos de implementación.</span><span class="sxs-lookup"><span data-stu-id="59c34-120">Modify the time-out period and retry count values in the implementation's database.</span></span> <span data-ttu-id="59c34-121">Para obtener más información, consulte [cambiar la Directiva de retransmisión](changing-the-retransmission-policy.md).</span><span class="sxs-lookup"><span data-stu-id="59c34-121">For more information, see [Changing the Retransmission Policy](changing-the-retransmission-policy.md).</span></span>
-   <span data-ttu-id="59c34-122">Llame a la función [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) para cancelar el ciclo de retransmisión y liberar las estructuras de datos internas asociadas a una única solicitud de mensaje SNMP.</span><span class="sxs-lookup"><span data-stu-id="59c34-122">Call the [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) function to cancel the retransmission cycle and release internal data structures associated with a single SNMP message request.</span></span> <span data-ttu-id="59c34-123">Para obtener más información, consulte cancelación de la [retransmisión](canceling-retransmission.md).</span><span class="sxs-lookup"><span data-stu-id="59c34-123">For more information, see [Canceling Retransmission](canceling-retransmission.md).</span></span>

<span data-ttu-id="59c34-124">La aplicación puede ejecutar su propia Directiva de retransmisión.</span><span class="sxs-lookup"><span data-stu-id="59c34-124">The application can execute its own retransmission policy.</span></span> <span data-ttu-id="59c34-125">En este caso, la ejecución puede o no basarse en los valores de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="59c34-125">In this case, execution may or may not be based on the values in the database.</span></span>

 

 




