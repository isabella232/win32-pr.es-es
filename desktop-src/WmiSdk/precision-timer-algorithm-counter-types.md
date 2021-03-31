---
description: Los tipos de contador del algoritmo del temporizador de precisión obtienen lecturas más precisas que los temporizadores del sistema.
ms.assetid: f7159645-6287-47a3-895e-20dae6e0892a
ms.tgt_platform: multiple
title: Tipos de contador del algoritmo de temporizador de precisión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3a8864587fedc915678dfa4a9e578ca051e1262
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818051"
---
# <a name="precision-timer-algorithm-counter-types"></a><span data-ttu-id="6ce35-103">Tipos de contador del algoritmo de temporizador de precisión</span><span class="sxs-lookup"><span data-stu-id="6ce35-103">Precision Timer Algorithm Counter Types</span></span>

<span data-ttu-id="6ce35-104">Los tipos de contador del algoritmo del temporizador de precisión obtienen lecturas más precisas que los temporizadores del sistema.</span><span class="sxs-lookup"><span data-stu-id="6ce35-104">The precision timer algorithm counter types obtain more accurate readings than system timers.</span></span> <span data-ttu-id="6ce35-105">El servicio que proporciona los datos también proporciona una marca de tiempo, que elimina los errores que pueden producirse debido a la hora pequeña y variable que transcurre entre la captura de la marca de tiempo del sistema y la recopilación de los datos del archivo DLL de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="6ce35-105">The service that provides the data also provides a timestamp, which eliminates the errors that can occur because of the small and variable time that elapses between capture of the system timestamp and collection of the data from the performance DLL.</span></span> <span data-ttu-id="6ce35-106">Esta marca de tiempo base para los temporizadores de precisión es una \_ propiedad timestamp de precisión de rendimiento \_ , que debe seguir inmediatamente a la \_ propiedad temporizador de precisión de rendimiento \_ .</span><span class="sxs-lookup"><span data-stu-id="6ce35-106">This base timestamp for precision timers is a PERF\_PRECISION\_TIMESTAMP property, which must immediately follow the PERF\_PRECISION\_TIMER property.</span></span>



| <span data-ttu-id="6ce35-107">Contratipo (constante)</span><span class="sxs-lookup"><span data-stu-id="6ce35-107">CounterType Constant</span></span>                                                                                         | <span data-ttu-id="6ce35-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="6ce35-108">Description</span></span>                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ce35-109">[Rendimiento \_ de Decimal \_ del \_ temporizador de precisión](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))541525248</span><span class="sxs-lookup"><span data-stu-id="6ce35-109">[PERF\_PRECISION\_SYSTEM\_TIMER](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 541525248</span></span><br/> | <span data-ttu-id="6ce35-110">Similar al \_ temporizador de contadores de rendimiento \_ , salvo que usa una base de tiempo definida por el contador en lugar de la marca de tiempo del sistema.</span><span class="sxs-lookup"><span data-stu-id="6ce35-110">Similar to PERF\_COUNTER\_TIMER except that it uses a counter defined time base instead of the system timestamp.</span></span>             |
| <span data-ttu-id="6ce35-111">[Rendimiento \_ de Decimal \_ \_ del temporizador de precisión de 100](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))542573824</span><span class="sxs-lookup"><span data-stu-id="6ce35-111">[PERF\_PRECISION\_100NS\_TIMER](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 542573824</span></span><br/>  | <span data-ttu-id="6ce35-112">Similar al temporizador de 100NSEC de rendimiento \_ \_ , salvo que usa una base de tiempo definida por un contador de 100 NS en lugar de la marca de tiempo de 100 ns del sistema.</span><span class="sxs-lookup"><span data-stu-id="6ce35-112">Similar to PERF\_100NSEC\_TIMER except that it uses a 100ns counter defined time base instead of the system 100ns timestamp.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="6ce35-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6ce35-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ce35-114">Tipos de contador de rendimiento de WMI</span><span class="sxs-lookup"><span data-stu-id="6ce35-114">WMI Performance Counter Types</span></span>](wmi-performance-counter-types.md)
</dt> </dl>

 

