---
description: Glosario de términos de Monitor de red que comienzan por la letra C.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9e0b9f77-8a47-4724-b08c-fac3b6e23afc
title: C (Monitor de red)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b06dd8ccd4d4c3382e7f7f7bb4426320bfcd8d4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652662"
---
# <a name="c-network-monitor"></a><span data-ttu-id="5eaf2-103">C (Monitor de red)</span><span class="sxs-lookup"><span data-stu-id="5eaf2-103">C (Network Monitor)</span></span>

<dl> <dt>

<span data-ttu-id="5eaf2-104"><span id="_netmon_capture_gly"></span><span id="_NETMON_CAPTURE_GLY"></span>**grabar**</span><span class="sxs-lookup"><span data-stu-id="5eaf2-104"><span id="_netmon_capture_gly"></span><span id="_NETMON_CAPTURE_GLY"></span>**capture**</span></span>
</dt> <dd>

<span data-ttu-id="5eaf2-105">Datos de tráfico de red que se recopilan en marcos.</span><span class="sxs-lookup"><span data-stu-id="5eaf2-105">Network traffic data that is collected in frames.</span></span> <span data-ttu-id="5eaf2-106">Un proveedor de paquetes de red (NPP) realiza una captura.</span><span class="sxs-lookup"><span data-stu-id="5eaf2-106">A network packet provider (NPP) performs a capture.</span></span> <span data-ttu-id="5eaf2-107">Vea también [*captura retrasada*](d.md)y *captura en tiempo real*</span><span class="sxs-lookup"><span data-stu-id="5eaf2-107">See also [*delayed capture*](d.md), and *real-time capture*</span></span>

</dd> <dt>

<span data-ttu-id="5eaf2-108"><span id="_netmon_capture_file_gly"></span><span id="_NETMON_CAPTURE_FILE_GLY"></span>**archivo de captura**</span><span class="sxs-lookup"><span data-stu-id="5eaf2-108"><span id="_netmon_capture_file_gly"></span><span id="_NETMON_CAPTURE_FILE_GLY"></span>**capture file**</span></span>
</dt> <dd>

<span data-ttu-id="5eaf2-109">Archivo que Monitor de red crea para almacenar los datos capturados.</span><span class="sxs-lookup"><span data-stu-id="5eaf2-109">A file that Network Monitor creates to store captured data.</span></span> <span data-ttu-id="5eaf2-110">La extensión de nombre de archivo. Cap identifica un archivo de captura.</span><span class="sxs-lookup"><span data-stu-id="5eaf2-110">The .cap file name extension identifies a capture file.</span></span> <span data-ttu-id="5eaf2-111">Monitor de red genera aleatoriamente un nombre de archivo de captura, pero puede cambiar el nombre de archivo al guardar el archivo de captura.</span><span class="sxs-lookup"><span data-stu-id="5eaf2-111">Network Monitor randomly generates a capture file name, but you can change the file name when you save the capture file.</span></span>

<span data-ttu-id="5eaf2-112">Monitor de red crea un archivo de captura cada vez que se inicia el proceso de captura y, a continuación, mantiene el archivo abierto durante el proceso de captura.</span><span class="sxs-lookup"><span data-stu-id="5eaf2-112">Network Monitor creates a capture file each time the capture process starts, and then keeps the file open during the capture process.</span></span> <span data-ttu-id="5eaf2-113">No se puede tener acceso al contenido de un archivo de captura hasta que el proceso de captura se detenga y se cierre el archivo de captura.</span><span class="sxs-lookup"><span data-stu-id="5eaf2-113">You cannot access the contents of a capture file until the capture process is stopped and the capture file is closed.</span></span>

</dd> <dt>

<span data-ttu-id="5eaf2-114"><span id="_netmon_capture_filter_gly"></span><span id="_NETMON_CAPTURE_FILTER_GLY"></span>**filtro de captura**</span><span class="sxs-lookup"><span data-stu-id="5eaf2-114"><span id="_netmon_capture_filter_gly"></span><span id="_NETMON_CAPTURE_FILTER_GLY"></span>**capture filter**</span></span>
</dt> <dd>

<span data-ttu-id="5eaf2-115">Conjunto de funciones de Monitor de red que se usan para restringir los fotogramas entrantes que usa una aplicación de proveedor de paquetes de red (NPP).</span><span class="sxs-lookup"><span data-stu-id="5eaf2-115">A set of Network Monitor functions used to restrict incoming frames that a network packet provider (NPP) application uses.</span></span>

</dd> <dt>

<span data-ttu-id="5eaf2-116"><span id="_netmon_capture_trigger_gly"></span><span id="_NETMON_CAPTURE_TRIGGER_GLY"></span>**desencadenador de captura**</span><span class="sxs-lookup"><span data-stu-id="5eaf2-116"><span id="_netmon_capture_trigger_gly"></span><span id="_NETMON_CAPTURE_TRIGGER_GLY"></span>**capture trigger**</span></span>
</dt> <dd>

<span data-ttu-id="5eaf2-117">Un evento de desencadenador que se establece para detener el proceso de captura.</span><span class="sxs-lookup"><span data-stu-id="5eaf2-117">A trigger event that is set to stop the capture process.</span></span> <span data-ttu-id="5eaf2-118">El evento de desencadenador de captura puede ser un archivo de captura temporal que se dirige a un nivel específico o a un patrón de datos que se produce en un fotograma capturado.</span><span class="sxs-lookup"><span data-stu-id="5eaf2-118">The capture trigger event can be a temporary capture file that is directed to a specific level or data pattern that occurs in a captured frame.</span></span>

</dd> <dt>

<span data-ttu-id="5eaf2-119"><span id="_netmon_captured_data_gly"></span><span id="_NETMON_CAPTURED_DATA_GLY"></span>**datos capturados**</span><span class="sxs-lookup"><span data-stu-id="5eaf2-119"><span id="_netmon_captured_data_gly"></span><span id="_NETMON_CAPTURED_DATA_GLY"></span>**captured data**</span></span>
</dt> <dd>

<span data-ttu-id="5eaf2-120">Fotogramas que tienen un conjunto definido de criterios.</span><span class="sxs-lookup"><span data-stu-id="5eaf2-120">Frames that have a defined set of criteria.</span></span> <span data-ttu-id="5eaf2-121">Las tramas de datos están contenidas en un archivo de captura temporal.</span><span class="sxs-lookup"><span data-stu-id="5eaf2-121">The data frames are contained in a temporary capture file.</span></span>

</dd> <dt>

<span data-ttu-id="5eaf2-122"><span id="_netmon_conversation_statistics_gly"></span><span id="_NETMON_CONVERSATION_STATISTICS_GLY"></span>**estadísticas de conversación**</span><span class="sxs-lookup"><span data-stu-id="5eaf2-122"><span id="_netmon_conversation_statistics_gly"></span><span id="_NETMON_CONVERSATION_STATISTICS_GLY"></span>**conversation statistics**</span></span>
</dt> <dd>

<span data-ttu-id="5eaf2-123">Estadísticas del tráfico de red que se guarda durante una captura.</span><span class="sxs-lookup"><span data-stu-id="5eaf2-123">Statistics of network traffic saved during a capture.</span></span> <span data-ttu-id="5eaf2-124">Estas estadísticas incluyen información de estación y de sesión que comienza cuando se inicia el proceso de captura y termina cuando se detiene la captura.</span><span class="sxs-lookup"><span data-stu-id="5eaf2-124">These statistics include station and session information beginning when the capture process starts, and ending when the capture stops.</span></span> <span data-ttu-id="5eaf2-125">Si pausa el proceso de captura, Monitor de red continúa agregando estadísticas al reanudar el proceso.</span><span class="sxs-lookup"><span data-stu-id="5eaf2-125">If you pause the capture process, Network Monitor continues to add statistics when you resume the process.</span></span> <span data-ttu-id="5eaf2-126">Para recuperar las estadísticas de conversación, llame al método **GetConversationStatistics** para la interfaz que está usando.</span><span class="sxs-lookup"><span data-stu-id="5eaf2-126">To retrieve conversation statistics, call the **GetConversationStatistics** method for the interface you are using.</span></span>

</dd> </dl>

 

 



