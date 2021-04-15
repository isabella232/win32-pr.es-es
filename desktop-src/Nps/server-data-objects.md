---
title: Objetos de datos del servidor
description: La API de objetos de datos del servidor (SDO) permite configurar y administrar mediante programación un sistema que ejecuta NPS.
ms.assetid: 9d159e15-f534-4ab1-9641-db70064beb51
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eebd0f837f9a8a36af1eb9118189015e677e2af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676425"
---
# <a name="server-data-objects"></a>Objetos de datos del servidor

> [!Note]  
> Se ha cambiado el nombre del servicio de autenticación de Internet (IAS) a partir de Windows Server 2008. El contenido de este tema se aplica a IAS y NPS. En todo el texto, NPS se usa para hacer referencia a todas las versiones del servicio, incluidas las versiones mencionadas originalmente como IAS.

 

La API de objetos de datos del servidor (SDO) permite configurar y administrar mediante programación un sistema que ejecuta NPS. Con SDO, un programador también puede escribir aplicaciones que administren directivas de acceso remoto y perfiles. Los perfiles y directivas de acceso remoto se usan en el servicio de enrutamiento y acceso remoto (RRAS), así como en NPS para determinar si un cliente remoto puede conectarse a un servidor de acceso a la red (NAS).

La API SDO es aplicable en cualquier entorno que use directivas de acceso remoto o NPS.

Con la API SDO, un desarrollador puede manipular cualquier elemento de la configuración de NPS que sea accesible a través de la interfaz de usuario de NPS.

La API SDO también permite establecer o recuperar cualquiera de los valores accesibles a través de la página de propiedades configuración de marcado del usuario.

La API SDO se compone de interfaces COM. Cada una de las interfaces de la API de SDO hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) de com. La interfaz **IDispatch** permite a los desarrolladores llamar a los métodos de interfaz SDO desde Visual Basic o cualquier cliente de automatización, así como desde C/C++.

Los desarrolladores también pueden llamar a la API SDO desde lenguajes de scripting como VBScript. Sin embargo, dado que VBScript está limitado a usar solo parámetros de tipo variante, no toda la funcionalidad de SDO está disponible.

## <a name="in-this-section"></a>En esta sección

[Información general](/windows/desktop/Nps/sdo-about-server-data-objects)

Información general sobre la API de objetos de datos del servidor.

[Utilizan](/windows/desktop/Nps/sdo-using-server-data-objects)

Código de ejemplo que muestra cómo usar la API de objetos de datos del servidor.

[Referencia](/windows/desktop/Nps/sdo-server-data-objects-reference)

Documentación de los tipos e interfaces enumerados que componen la API de objetos de datos del servidor.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Servidor de directivas de redes (servicio de autenticación de Internet)](portal.md)
</dt> <dt>

[Servicio de acceso remoto](/windows/desktop/RRAS/portal)
</dt> </dl>

 

 