---
title: Objetos de datos de servidor
description: La API de objetos de datos de servidor (SDO) permite configurar y administrar mediante programación un sistema que ejecuta NPS.
ms.assetid: 9d159e15-f534-4ab1-9641-db70064beb51
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eebd0f837f9a8a36af1eb9118189015e677e2af
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127245072"
---
# <a name="server-data-objects"></a>Objetos de datos de servidor

> [!Note]  
> El nombre del Servicio de autenticación de Internet (IAS) se ha cambiado a Servidor de directivas de red (NPS) a partir Windows Server 2008. El contenido de este tema se aplica a IAS y NPS. A lo largo del texto, NPS se usa para hacer referencia a todas las versiones del servicio, incluidas las versiones a las que se hizo referencia originalmente como IAS.

 

La API de objetos de datos de servidor (SDO) permite configurar y administrar mediante programación un sistema que ejecuta NPS. Con SDO, un desarrollador también puede escribir aplicaciones que administran perfiles y directivas de acceso remoto. El servicio de enrutamiento y acceso remoto (RRAS), así como NPS, usan las directivas de acceso remoto y los perfiles para determinar si un cliente remoto puede conectarse a un servidor de acceso a la red (NAS).

La API de SDO es aplicable en cualquier entorno que use NPS o directivas de acceso remoto.

Con la API de SDO, un desarrollador puede manipular cualquier elemento de la configuración de NPS al que se pueda acceder a través de la interfaz de usuario de NPS.

La API de SDO también permite establecer o recuperar cualquiera de los valores accesibles a través de la página de propiedades de configuración de acceso telefónico del usuario.

La API de SDO se compone de interfaces COM. Cada una de las interfaces de la API de SDO hereda de la [**interfaz IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) com. La **interfaz IDispatch** permite a los desarrolladores llamar a los métodos de interfaz SDO desde Visual Basic o cualquier cliente de Automation, así como desde C/C++.

Los desarrolladores también pueden llamar a la API de SDO desde lenguajes de scripting como VBScript. Sin embargo, dado que VBScript se limita a usar solo parámetros de tipo VARIANT, no toda la funcionalidad de SDO está disponible.

## <a name="in-this-section"></a>En esta sección

[Información general](/windows/desktop/Nps/sdo-about-server-data-objects)

Información general sobre Server Data Objects API.

[Usando](/windows/desktop/Nps/sdo-using-server-data-objects)

Código de ejemplo que muestra cómo usar Server Data Objects API.

[Referencia](/windows/desktop/Nps/sdo-server-data-objects-reference)

Documentación de los tipos e interfaces enumerados que componen server data objects API.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Servidor de directivas de red (Servicio de autenticación de Internet)](portal.md)
</dt> <dt>

[Servicio de acceso remoto](/windows/desktop/RRAS/portal)
</dt> </dl>

 

 