---
title: Referencia del complemento
description: Funciones de adaptador, funciones de contenedor y estructuras para crear adaptadores de complementos personalizados de tres tipos de motor, sensor y almacenamiento.
ms.assetid: 1886c389-b914-4b2d-ab7e-3e163782673d
keywords:
- Windows Biometric Framework API Windows Biometric Framework API, referencia de complemento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2223f398579663d94c0cc40daef1fcf37e4239d8d0dc8246fedd15b454b3354
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119410965"
---
# <a name="plug-in-reference"></a>Referencia del complemento

Los dispositivos biométricos se fabrica en una amplia variedad de tipos y configuraciones. El Windows Biometric Framework incorpora una arquitectura extensible que le permite tratar esta variedad mediante la creación de complementos personalizados. En el centro de esta arquitectura se encuentra un objeto de software denominado unidad biométrica. Puede pensar en una unidad biométrica como una abstracción que representa un dispositivo biométrico para framework. Los componentes de software de complemento denominados adaptadores conectan la unidad biométrica al hardware asociado. Hay tres tipos de adaptadores que puede crear. Un adaptador de motor genera plantillas biométricas a partir de ejemplos capturados, coincide con las plantillas existentes e indexa las plantillas. Un adaptador de sensor encapsula un dispositivo biométrico y proporciona una interfaz estándar para configurar el sensor, capturar muestras y controlar el flujo de datos biométricos al motor de procesamiento. Un adaptador de almacenamiento administra las bases de datos de plantilla.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                 | Descripción                                                                                                                                                        |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Funciones de complemento](plug-in-functions.md)<br/>                 | Funciones que puede usar para crear los complementos de adaptador que crean una unidad biométrica.<br/>                                                                     |
| [Estructuras de complemento](plug-in-structures.md)<br/>               | Estructuras para el desarrollo de aplicaciones cliente mediante Windows Biometric Framework API.<br/>                                                                   |
| [Funciones contenedoras de complementos](plug-in-wrapper-functions.md)<br/> | Funciones contenedoras que permiten llamar a una función pública en cualquier adaptador asociado a la canalización sin adquirir manualmente un puntero al adaptador.<br/> |



 

 

 





