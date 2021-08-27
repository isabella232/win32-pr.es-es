---
description: En esta sección se proporciona una lista de los códigos de retorno de WMI, constantes simbólicas, valores literales y descripciones. Estos códigos pueden devolverse mediante scripts, aplicaciones de C++ o comandos Wmic.
ms.assetid: 7ae47482-edf4-4aa4-858a-76e55f3cb0a3
ms.tgt_platform: multiple
title: Códigos de retorno wmi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1454c8efc45085e88f78358346679b5cdcf3d05093318845912d7d5a913d8ecf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995385"
---
# <a name="wmi-return-codes"></a>Códigos de retorno wmi

En esta sección se proporciona una lista de los códigos de retorno de WMI, constantes simbólicas, valores literales y descripciones. Estos códigos pueden devolverse mediante scripts, aplicaciones de C++ o [**comandos Wmic.**](wmic.md)

Si se produce un error, WMI devuelve uno de los siguientes códigos de error como un valor de 32 bits donde los dos bits de orden superior indican el código de gravedad del mensaje.

<dl> <dt>

<span id="0"></span>0
</dt> <dd>

Correcto

</dd> <dt>

<span id="1"></span>1
</dt> <dd>

Informativo

</dd> <dt>

<span id="2"></span>2
</dt> <dd>

Advertencia

</dd> <dt>

<span id="3"></span>3
</dt> <dd>

Error

</dd> </dl>

> [!Note]
>
> Si WMI devuelve mensajes de error, tenga en cuenta que es posible que no indiquen problemas en el servicio WMI o en los proveedores WMI. Los errores pueden originarse en otras partes del sistema operativo y surgir como errores a través de WMI. En cualquier caso, no elimine el repositorio WMI como primera acción porque la eliminación del repositorio puede causar daños en el sistema o en las aplicaciones instaladas.
>
> Para obtener más información sobre el origen del problema, puede descargar y ejecutar la Utilidad de diagnóstico de WMI [línea](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) de comandos de diagnóstico. Esta herramienta genera un informe que normalmente puede aislar el origen del problema y proporcionar instrucciones sobre cómo corregirlo. El informe también ayuda a los servicios de soporte técnico de Microsoft a ayudarle. Puede descargar la Utilidad de diagnóstico de WMI [aquí.](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d)

 

-   [**Constantes de error wmi**](wmi-error-constants.md)
-   [**Constantes wmi sin errores**](wmi-non-error-constants.md)

 

 



