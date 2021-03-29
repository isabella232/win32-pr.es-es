---
title: Referencia del complemento
description: 'Funciones de adaptador, funciones de contenedor y estructuras para crear adaptadores de complementos personalizados de tres tipos: motor, sensor y almacenamiento.'
ms.assetid: 1886c389-b914-4b2d-ab7e-3e163782673d
keywords:
- API de API Plataforma de biometría de Windows de Plataforma de biometría de Windows, referencia del complemento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc764be98f6417d211effe1c182279d54c95d234
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104487014"
---
# <a name="plug-in-reference"></a>Referencia del complemento

Los dispositivos biométricos se fabrican en una amplia variedad de tipos y configuraciones. La Plataforma de biometría de Windows incorpora una arquitectura extensible que permite tratar con esta variedad mediante la creación de complementos personalizados. En el centro de esta arquitectura hay un objeto de software denominado unidad biométrica. Puede pensar en una unidad biométrica como una abstracción que representa un dispositivo biométrico en el marco. Los componentes de software de complemento denominados adaptadores conectan la unidad biométrica al hardware asociado. Hay tres tipos de adaptadores que puede crear. Un adaptador de motor genera plantillas biométricas a partir de ejemplos capturados, coincide con ejemplos con plantillas existentes e indexa plantillas. Un adaptador de sensor encapsula un dispositivo biométrico y proporciona una interfaz estándar para configurar el sensor, capturar ejemplos y controlar el flujo de datos biométricos al motor de procesamiento. Un adaptador de almacenamiento administra las bases de datos de plantilla.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                 | Descripción                                                                                                                                                        |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Funciones de complemento](plug-in-functions.md)<br/>                 | Funciones que puede usar para crear los complementos de adaptador que componen una unidad biométrica.<br/>                                                                     |
| [Estructuras de complementos](plug-in-structures.md)<br/>               | Estructuras para el desarrollo de aplicaciones cliente mediante la API de Plataforma de biometría de Windows.<br/>                                                                   |
| [Funciones de contenedor de complementos](plug-in-wrapper-functions.md)<br/> | Funciones contenedoras que permiten llamar a una función pública en cualquier adaptador conectado a la canalización sin adquirir manualmente un puntero al adaptador.<br/> |



 

 

 





