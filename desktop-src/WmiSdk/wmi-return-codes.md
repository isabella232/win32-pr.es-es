---
description: En esta sección se proporciona una lista de los códigos de retorno, las constantes simbólicas, los valores literales y las descripciones de WMI. Estos códigos pueden ser devueltos por scripts, aplicaciones de C++ o comandos de WMIC.
ms.assetid: 7ae47482-edf4-4aa4-858a-76e55f3cb0a3
ms.tgt_platform: multiple
title: Códigos de retorno de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e05455b109bd05b7a1693b8a05b13f6f7aeb646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696779"
---
# <a name="wmi-return-codes"></a>Códigos de retorno de WMI

En esta sección se proporciona una lista de los códigos de retorno, las constantes simbólicas, los valores literales y las descripciones de WMI. Estos códigos pueden ser devueltos por scripts, aplicaciones de C++ o comandos de [**WMIC**](wmic.md) .

Si se produce un error, WMI devuelve uno de los siguientes códigos de error como un valor de 32 bits en el que los dos bits de orden superior indican el código de gravedad del mensaje.

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
> Si WMI devuelve mensajes de error, tenga en cuenta que es posible que no indiquen problemas en el servicio WMI o en los proveedores WMI. Los errores pueden originarse en otras partes del sistema operativo y surgir como errores a través de WMI. En cualquier circunstancia, no elimine el repositorio WMI como primera acción, ya que la eliminación del repositorio puede provocar daños en el sistema o en las aplicaciones instaladas.
>
> Para obtener más información sobre el origen del problema, puede descargar y ejecutar la herramienta de línea de comandos de diagnóstico de [utilidad de diagnóstico de WMI](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) . Esta herramienta genera un informe que normalmente puede aislar el origen del problema y proporcionar instrucciones sobre cómo corregirlo. El informe también ayuda a los servicios de soporte técnico de Microsoft para ayudarle. Puede descargar el Utilidad de diagnóstico de WMI [aquí](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).

 

-   [**Constantes de error de WMI**](wmi-error-constants.md)
-   [**Constantes que no son de error de WMI**](wmi-non-error-constants.md)

 

 



