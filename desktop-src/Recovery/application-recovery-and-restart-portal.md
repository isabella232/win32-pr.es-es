---
title: Recuperación y reinicio de aplicaciones
description: Escriba instaladores personalizados para reiniciar automáticamente una aplicación que se ha cerrado para completar una actualización. Guarde los datos y configure la recuperación de aplicaciones antes de salir de los programas.
ms.assetid: 60b057dd-9724-4bc4-b1b0-eea7e8380ecb
keywords:
- restart
- recover
- recovery
- confiabilidad
- confiabilidad de software
- recuperación de aplicaciones
- reinicio de la aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d31d6c8ef342b9e1781297d547358317a90d515002e6ef3e529b8d7a0c50aa09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024605"
---
# <a name="application-recovery-and-restart"></a>Recuperación y reinicio de aplicaciones

## <a name="purpose"></a>Propósito

Una aplicación puede usar Recuperación y reinicio de aplicaciones (ARR) para guardar datos y información de estado antes de que la aplicación se cierre debido a una excepción no controlada o cuando la aplicación deje de responder. La aplicación también se reinicia, si se solicita.

También se puede reiniciar una aplicación si un instalador actualiza un componente de la aplicación o si el equipo necesita reiniciarse como resultado de una actualización. Tenga en cuenta que para admitir el reinicio automático de la aplicación después de que un instalador actualice una aplicación, tanto la aplicación como el instalador deben crearse correctamente. Para más información, consulte [Registro para el reinicio de la aplicación.](registering-for-application-restart.md)

## <a name="developer-audience"></a>Audiencia de desarrolladores

ARR está diseñado para desarrolladores de C y C++.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

ARR está disponible a partir del sistema operativo Windows Vista.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                   | Descripción                                                           |
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Uso de la recuperación y el reinicio de aplicaciones](using-application-recovery-and-restart.md)<br/>         | Guía de procedimientos para registrarse para la recuperación y el reinicio.<br/> |
| [Referencia de recuperación y reinicio de aplicaciones](application-recovery-and-restart-reference.md)<br/> | Información de referencia de la API de ARR. <br/>                    |



 

 

 





