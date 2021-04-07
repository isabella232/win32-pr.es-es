---
title: Recuperación y reinicio de aplicaciones
description: Escriba instaladores personalizados para reiniciar automáticamente una aplicación que se ha cerrado para completar una actualización. Guarde los datos y configure la recuperación de la aplicación antes de salir de los programas.
ms.assetid: 60b057dd-9724-4bc4-b1b0-eea7e8380ecb
keywords:
- restart
- recover
- recovery
- confiabilidad
- confiabilidad del software
- recuperación de aplicaciones
- reinicio de la aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 862236fad876307b0662a8444775c78673b92983
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903803"
---
# <a name="application-recovery-and-restart"></a>Recuperación y reinicio de aplicaciones

## <a name="purpose"></a>Propósito

Una aplicación puede usar la recuperación y el reinicio de la aplicación (ARR) para guardar los datos y la información de estado antes de que se cierre la aplicación debido a una excepción no controlada o cuando la aplicación deja de responder. También se reinicia la aplicación, si se solicita.

También se puede reiniciar una aplicación si un instalador actualiza un componente de la aplicación, o si el equipo tiene que reiniciarse como resultado de una actualización. Tenga en cuenta que para admitir el reinicio automático de aplicaciones después de que un instalador actualice una aplicación, la aplicación y el instalador deben crearse de forma adecuada. Para obtener más información, consulte [registro del reinicio de la aplicación](registering-for-application-restart.md).

## <a name="developer-audience"></a>Audiencia de desarrolladores

ARR está diseñado para desarrolladores de C y C++.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

ARR está disponible a partir del sistema operativo Windows Vista.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                   | Descripción                                                           |
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Uso de la recuperación y reinicio de aplicaciones](using-application-recovery-and-restart.md)<br/>         | Guía de procedimientos para el registro para recuperación y reinicio.<br/> |
| [Referencia de recuperación y reinicio de aplicaciones](application-recovery-and-restart-reference.md)<br/> | Información de referencia para la API de ARR. <br/>                    |



 

 

 





