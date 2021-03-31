---
title: Configuración de secuencias arbitrarias personalizadas
description: Configuración de secuencias arbitrarias personalizadas
ms.assetid: 09b28fd3-a0a3-44d9-b664-7421290abf02
keywords:
- flujos, configurar secuencias arbitrarias personalizadas
- códecs, configurar secuencias arbitrarias personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29d5cf3e95a5514ddeede9eb3c25df01ed4cd2ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775697"
---
# <a name="configuring-custom-arbitrary-streams"></a><span data-ttu-id="49106-105">Configuración de secuencias arbitrarias personalizadas</span><span class="sxs-lookup"><span data-stu-id="49106-105">Configuring Custom Arbitrary Streams</span></span>

<span data-ttu-id="49106-106">Al usar su propio tipo de datos arbitrario, debe crear un valor de GUID para que sirva como el identificador de tipo de medio principal para él.</span><span class="sxs-lookup"><span data-stu-id="49106-106">When using your own arbitrary data type, you must create a GUID value to serve as the major media type identifier for it.</span></span> <span data-ttu-id="49106-107">Cuando el escritor encuentra una secuencia en un perfil con un tipo principal que no reconoce, se supone que la secuencia son datos arbitrarios personalizados.</span><span class="sxs-lookup"><span data-stu-id="49106-107">When the writer encounters a stream in a profile with a major type it does not recognize, it assumes that the stream is custom arbitrary data.</span></span> <span data-ttu-id="49106-108">Aceptará sus ejemplos, los pondrá en paquetes y los combinará con ejemplos de las otras secuencias del archivo sin comprobar de ningún modo los datos.</span><span class="sxs-lookup"><span data-stu-id="49106-108">It will accept your samples, packetize them, and combine them with samples from the other streams in the file without verifying the data in any way.</span></span>

<span data-ttu-id="49106-109">También puede crear sus propios identificadores GUID de subtipos para definir subcategorías de los datos personalizados.</span><span class="sxs-lookup"><span data-stu-id="49106-109">You can also create your own subtype GUID identifiers to define subcategories of your custom data.</span></span> <span data-ttu-id="49106-110">El escritor omitirá todos estos subtipos por completo, pero se conservarán en la sección de encabezado del archivo ASF, de modo que la aplicación de lectura pueda recuperarlos y tomar decisiones basadas en ellos.</span><span class="sxs-lookup"><span data-stu-id="49106-110">The writer will ignore these subtypes completely, but they will be preserved in the header section of the ASF file, so your reading application can retrieve them and make decisions based on them.</span></span>

<span data-ttu-id="49106-111">Una secuencia arbitraria requiere una ventana de velocidad de bits y de búfer, y debe tener una estructura de [**\_ \_ tipo de medio de WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) con los valores borrados, excepto el tipo de medio principal y el subtipo (si se usa uno).</span><span class="sxs-lookup"><span data-stu-id="49106-111">An arbitrary stream requires a bit rate and buffer window, and must have a [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure with the values cleared except for the major media type and subtype(if using one).</span></span>

## <a name="related-topics"></a><span data-ttu-id="49106-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="49106-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49106-113">**Configuración común para todos los flujos**</span><span class="sxs-lookup"><span data-stu-id="49106-113">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="49106-114">**Configuración de tipos de flujo arbitrarios**</span><span class="sxs-lookup"><span data-stu-id="49106-114">**Configuring Arbitrary Stream Types**</span></span>](configuring-arbitrary-stream-types.md)
</dt> <dt>

[<span data-ttu-id="49106-115">**Flujos de datos arbitrarios personalizados**</span><span class="sxs-lookup"><span data-stu-id="49106-115">**Custom Arbitrary Data Streams**</span></span>](custom-arbitrary-data-streams.md)
</dt> </dl>

 

 




