---
description: La capa de datos suele contener información más estática&\# 8212; información conservada en un medio duradero.
ms.assetid: d2bce8b6-1f88-4e4a-bb08-fc7ee4c039da
title: Optimizar las llamadas entre la lógica de negocios y los datos de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3346f628344e7505fde03c3a64b7420d199312ee
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705300"
---
# <a name="optimizing-interactions-between-the-com-business-logic-tier-and-the-data-tier"></a><span data-ttu-id="d66d1-103">Optimizar las interacciones entre el nivel de lógica empresarial de COM+ y el nivel de datos</span><span class="sxs-lookup"><span data-stu-id="d66d1-103">Optimizing Interactions Between the COM+ Business Logic Tier and the Data Tier</span></span>

<span data-ttu-id="d66d1-104">La capa de datos suele contener información más estática: información conservada en un medio duradero.</span><span class="sxs-lookup"><span data-stu-id="d66d1-104">The data tier often contains mostly static information—information persisted on durable media.</span></span> <span data-ttu-id="d66d1-105">Dado que este nivel engloba información que es principalmente estática, requiere un análisis exhaustivo de los posibles cuellos de botella.</span><span class="sxs-lookup"><span data-stu-id="d66d1-105">Because this tier encompasses information that is mostly static, it requires a thorough analysis for potential bottlenecks.</span></span> <span data-ttu-id="d66d1-106">Además de la posibilidad obvia de los cuellos de botella de conexión, las zonas activas pueden estar causadas por registros de acceso frecuente, métodos de acceso a datos ineficaces y la necesidad de coordinar el acceso a los sistemas heredados.</span><span class="sxs-lookup"><span data-stu-id="d66d1-106">In addition to the obvious possibility for connection bottlenecks, hot spots can be caused by frequently accessed records, inefficient data access methods, and the need to coordinate access to legacy systems.</span></span>

## <a name="connecting-to-the-data-tier"></a><span data-ttu-id="d66d1-107">Conexión a la capa de datos</span><span class="sxs-lookup"><span data-stu-id="d66d1-107">Connecting to the Data Tier</span></span>

<span data-ttu-id="d66d1-108">Dos consideraciones desempeñan un papel importante en el diseño de una capa de datos para una aplicación COM+: la agrupación de conexiones y la [activación Just-in-Time (JIT) de com+](com--just-in-time-activation.md)y el uso de DSN.</span><span class="sxs-lookup"><span data-stu-id="d66d1-108">Two considerations play an important role in designing a data tier for a COM+ application: connection pooling and [COM+ just-in-time (JIT) activation](com--just-in-time-activation.md), and the use of DSNs.</span></span> <span data-ttu-id="d66d1-109">Los componentes que realizan conexiones con la capa de datos deben usar la [agrupación de objetos com+](com--object-pooling.md) establecida en el componente.</span><span class="sxs-lookup"><span data-stu-id="d66d1-109">Components that make connections to the data tier should use [COM+ object pooling](com--object-pooling.md) set on the component.</span></span>

<span data-ttu-id="d66d1-110">Al crear los DSN, use las cadenas del constructor de objetos especificadas en el componente en lugar de crear un DSN de archivo.</span><span class="sxs-lookup"><span data-stu-id="d66d1-110">When creating DSNs, use object constructor strings specified on the component instead of creating a File DSN.</span></span> <span data-ttu-id="d66d1-111">Los DSN de archivo son más lentos que una conexión mediante una cadena de constructor de objeto.</span><span class="sxs-lookup"><span data-stu-id="d66d1-111">File DSNs are slower than a connection using an object constructor string.</span></span> <span data-ttu-id="d66d1-112">Las cadenas del constructor de objetos se pueden especificar en la hoja de propiedades del componente.</span><span class="sxs-lookup"><span data-stu-id="d66d1-112">Object constructor strings can be specified on the component property sheet.</span></span> <span data-ttu-id="d66d1-113">Para obtener más información, vea [cadenas del constructor de objetos com+](com--object-constructor-strings.md).</span><span class="sxs-lookup"><span data-stu-id="d66d1-113">For more information, see [COM+ Object Constructor Strings](com--object-constructor-strings.md).</span></span>

<span data-ttu-id="d66d1-114">Si usa componentes para tener acceso a una base de datos de SQL Server, utilice la agrupación de objetos COM+ en lugar de la agrupación de conexiones de SQL.</span><span class="sxs-lookup"><span data-stu-id="d66d1-114">If you are using components to access a SQL Server database, use COM+ object pooling instead of SQL connection pooling.</span></span>

<span data-ttu-id="d66d1-115">Si el componente usa ADO para capturar varios conjuntos de registros, establezca varias conexiones para el componente.</span><span class="sxs-lookup"><span data-stu-id="d66d1-115">If your component is using ADO to fetch multiple recordsets, establish multiple connections for the component.</span></span> <span data-ttu-id="d66d1-116">Cuando ADO Recupera varios conjuntos de registros, crea varias conexiones en segundo plano si no se crean.</span><span class="sxs-lookup"><span data-stu-id="d66d1-116">When ADO retrieves multiple recordsets, it creates multiple connections in the background if you do not create them.</span></span> <span data-ttu-id="d66d1-117">Si los crea, puede agruparlos y tener más control sobre el número de conexiones utilizadas.</span><span class="sxs-lookup"><span data-stu-id="d66d1-117">If you create them, you can pool them and have more control over the number of the connections used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d66d1-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d66d1-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d66d1-119">Optimizar las interacciones entre el nivel de lógica empresarial de COM+ y el nivel de presentación</span><span class="sxs-lookup"><span data-stu-id="d66d1-119">Optimizing Interactions Between the COM+ Business Logic Tier and the Presentation Tier</span></span>](optimizing-interactions-between-the-com--business-logic-tier-and-the-presentation-tier.md)
</dt> </dl>

 

 



