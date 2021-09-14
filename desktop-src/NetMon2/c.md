---
description: Glosario de Monitor de red términos que comienzan por la letra C.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9e0b9f77-8a47-4724-b08c-fac3b6e23afc
title: C (Monitor de red)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b06dd8ccd4d4c3382e7f7f7bb4426320bfcd8d4f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253928"
---
# <a name="c-network-monitor"></a>C (Monitor de red)

<dl> <dt>

<span id="_netmon_capture_gly"></span><span id="_NETMON_CAPTURE_GLY"></span>**capturar**
</dt> <dd>

Datos de tráfico de red que se recopilan en fotogramas. Un proveedor de paquetes de red (NPP) realiza una captura. Consulte también [*la captura retrasada*](d.md)y *la captura en tiempo real.*

</dd> <dt>

<span id="_netmon_capture_file_gly"></span><span id="_NETMON_CAPTURE_FILE_GLY"></span>**archivo de captura**
</dt> <dd>

Un archivo que Monitor de red para almacenar los datos capturados. La extensión de nombre de archivo .cap identifica un archivo de captura. Monitor de red genera aleatoriamente un nombre de archivo de captura, pero puede cambiar el nombre de archivo al guardar el archivo de captura.

Monitor de red crea un archivo de captura cada vez que se inicia el proceso de captura y, a continuación, mantiene el archivo abierto durante el proceso de captura. No se puede acceder al contenido de un archivo de captura hasta que se detenga el proceso de captura y se cierre el archivo de captura.

</dd> <dt>

<span id="_netmon_capture_filter_gly"></span><span id="_NETMON_CAPTURE_FILTER_GLY"></span>**filtro de captura**
</dt> <dd>

Un conjunto de Monitor de red funciones usadas para restringir los marcos entrantes que usa una aplicación de proveedor de paquetes de red (NPP).

</dd> <dt>

<span id="_netmon_capture_trigger_gly"></span><span id="_NETMON_CAPTURE_TRIGGER_GLY"></span>**desencadenador de captura**
</dt> <dd>

Evento de desencadenador que se establece para detener el proceso de captura. El evento de desencadenador de captura puede ser un archivo de captura temporal que se dirige a un nivel específico o a un patrón de datos que se produce en un fotograma capturado.

</dd> <dt>

<span id="_netmon_captured_data_gly"></span><span id="_NETMON_CAPTURED_DATA_GLY"></span>**datos capturados**
</dt> <dd>

Fotogramas que tienen un conjunto definido de criterios. Las tramas de datos están contenidas en un archivo de captura temporal.

</dd> <dt>

<span id="_netmon_conversation_statistics_gly"></span><span id="_NETMON_CONVERSATION_STATISTICS_GLY"></span>**estadísticas de conversación**
</dt> <dd>

Estadísticas del tráfico de red guardado durante una captura. Estas estadísticas incluyen información de estación y sesión que comienza cuando se inicia el proceso de captura y termina cuando se detiene la captura. Si pausa el proceso de captura, Monitor de red sigue agregando estadísticas al reanudar el proceso. Para recuperar las estadísticas de conversación, llame al **método GetConversationStatistics** para la interfaz que está usando.

</dd> </dl>

 

 



