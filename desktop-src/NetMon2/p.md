---
description: Glosario de términos de Monitor de red que comienzan por la letra P.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 321398fb-683f-4fb1-b6b7-c7826811cacd
title: P (Monitor de red)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44a95ed739acb6f4a59cf8c7a7edb760547f6469
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082223"
---
# <a name="p-network-monitor"></a>P (Monitor de red)

<dl> <dt>

<span id="_netmon_packet_gly"></span><span id="_NETMON_PACKET_GLY"></span>**paquete**
</dt> <dd>

Consulte [*Frame*](f.md).

</dd> <dt>

<span id="_netmon_parser_gly"></span><span id="_NETMON_PARSER_GLY"></span>**Analizador**
</dt> <dd>

Componente que detecta un protocolo específico en una captura retrasada. Cada analizador puede detectar un protocolo. Sin embargo, un archivo DLL de analizador puede contener varios analizadores. También se denomina analizador de protocolos.

</dd> <dt>

<span id="_netmon_parser.ini_gly"></span><span id="_NETMON_PARSER.INI_GLY"></span>**parser.ini**
</dt> <dd>

Un Monitor de red archivo de inicialización que contiene una lista de todos los analizadores instalados. Para cada analizador hay una cadena de comentario que describe el analizador, el siguiente conjunto del analizador y cualquier archivo de ayuda asociado con el analizador. El archivo INI del analizador se actualiza cuando Monitor de red llama a **ParserAutoInstallInfo**, o cuando el dll del analizador llama a **CreateHandoffTable**.

</dd> <dt>

<span id="_netmon_perfmon_gly"></span><span id="_NETMON_PERFMON_GLY"></span>**Contador**
</dt> <dd>

Herramienta de software que le permite ver las variables relacionadas con el rendimiento de la red que identifican la actividad de un proceso.

</dd> <dt>

<span id="_netmon_promiscuous_mode_gly"></span><span id="_NETMON_PROMISCUOUS_MODE_GLY"></span>**modo promiscuo**
</dt> <dd>

Estado en el que una tarjeta adaptadora de red copia todos los fotogramas que pasan a través de la red, independientemente de la dirección de destino a un búfer local. Este modo permite a Monitor de red capturar y mostrar todo el tráfico de red.

</dd> <dt>

<span id="_netmon_property_gly"></span><span id="_NETMON_PROPERTY_GLY"></span>**propiedad**
</dt> <dd>

Un elemento Protocol en un analizador que describe un campo de datos dentro de un marco que se envía mediante ese protocolo.

</dd> <dt>

<span id="_netmon_property_database_gly"></span><span id="_NETMON_PROPERTY_DATABASE_GLY"></span>**base de datos de propiedades**
</dt> <dd>

Base de datos interna que define todas las propiedades que admite un protocolo concreto. La base de datos de propiedades contiene una estructura **PROPERTYINFO** para cada propiedad que define el analizador. Monitor de red usa la información de la base de datos cuando adjunta una definición de propiedad a una instancia de la propiedad y cuando da formato a los datos de propiedad que se muestran en el panel de detalles de la interfaz de usuario de Monitor de red.

</dd> <dt>

<span id="_netmon_protocol_level_gly"></span><span id="_NETMON_PROTOCOL_LEVEL_GLY"></span>**nivel de protocolo**
</dt> <dd>

Agrupación lógica de propiedades de protocolo.

</dd> </dl>

 

 



