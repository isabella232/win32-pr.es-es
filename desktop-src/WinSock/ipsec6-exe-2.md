---
description: La configuración de directivas IPSec y asociaciones de seguridad para IPv6 se realiza con Ipsec6.exe.
ms.assetid: 9a0c8e48-bc57-461d-9ade-54b75f7aa56d
title: Ipsec6.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b373e8ab0dc54c3c8ee2fae8bc05722a9ac6aa64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715122"
---
# <a name="ipsec6exe"></a>Ipsec6.exe

La configuración de directivas IPSec y asociaciones de seguridad para IPv6 se realiza con Ipsec6.exe. A continuación se muestran los subcomandos Ipsec6.exe:

<dl> <dt>

<span id="ipsec6_sp__Interface_"></span><span id="ipsec6_sp__interface_"></span><span id="IPSEC6_SP__INTERFACE_"></span>de **IPSEC6 \[ SP** _Interfaz_ de *_\]_*
</dt> <dd>

Muestra las directivas de seguridad activas. Como alternativa, se muestran las directivas de seguridad activas para una interfaz específica.

</dd> <dt>

<span id="ipsec6_sa"></span><span id="IPSEC6_SA"></span>**IPSEC6 SA**
</dt> <dd>

Muestra las asociaciones de seguridad activas.

</dd> <dt>

<span id="ipsec6_c__FileName_without_extension__"></span><span id="ipsec6_c__filename_without_extension__"></span><span id="IPSEC6_C__FILENAME_WITHOUT_EXTENSION__"></span>**IPSEC6 c \[** _Nombre de archivo (sin extensión)_*_\]_*
</dt> <dd>

Crea archivos que se usan para configurar la Directiva de seguridad y las asociaciones de seguridad. Crea *filename*. SPD para las directivas de seguridad y *filename*. Sad para las asociaciones de seguridad. Use los archivos creados como plantillas para configurar las directivas de seguridad o las asociaciones de seguridad. Los archivos se pueden modificar con un editor de texto. Para invocar la configuración contenida en los archivos SPD y SAD, use el comando **IPSEC6 a** .

</dd> <dt>

<span id="ipsec6_a__FileName_without_extension__"></span><span id="ipsec6_a__filename_without_extension__"></span><span id="IPSEC6_A__FILENAME_WITHOUT_EXTENSION__"></span>**IPSEC6 a \[** _Nombre de archivo (sin extensión)_*_\]_*
</dt> <dd>

Agrega directivas de seguridad en *filename*. SPD y asociaciones de seguridad en *filename*. Sad a la lista de directivas de seguridad y asociaciones de seguridad activas.

</dd> <dt>

<span id="ipsec6_i__Policy___FileName_without_extension__"></span><span id="ipsec6_i__policy___filename_without_extension__"></span><span id="IPSEC6_I__POLICY___FILENAME_WITHOUT_EXTENSION__"></span>**IPSEC6 i \[** Nombre de archivo de _Directiva_ *_\] \[_* _(sin extensión)_*_\]_*
</dt> <dd>

Agrega directivas de seguridad en *filename*. SPD y asociaciones de seguridad en *filename*. Sad a la lista de directivas de seguridad activas y asociaciones de seguridad a las que hace referencia el número de la Directiva.

</dd> <dt>

<span id="ipsec6_d__type___sp_sa___IndexNumber_"></span><span id="ipsec6_d__type___sp_sa___indexnumber_"></span><span id="IPSEC6_D__TYPE___SP_SA___INDEXNUMBER_"></span>**IPSEC6 d \[ Type = SP SA \] \[** _IndexNumber_*_\]_*
</dt> <dd>

Elimina las directivas de seguridad o las asociaciones de seguridad de la lista de directivas de seguridad activas y asociaciones de seguridad, según el número de índice (que se muestra con **IPSEC6 SP** o **IPSEC6 SA**).

</dd> </dl>

 

 



