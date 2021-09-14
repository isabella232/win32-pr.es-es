---
description: Para recuperar datos del Registro, una aplicación enumera normalmente las subclaves de una clave hasta que encuentra una determinada y, a continuación, recupera los datos del valor o los valores asociados a ella.
ms.assetid: ce4be388-5506-4d01-a73c-33372ef4ccd7
title: Recuperar datos del Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45d8dd6f6e4d667cf2760c7cba441200755fb6c3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160679"
---
# <a name="retrieving-data-from-the-registry"></a>Recuperar datos del Registro

Para recuperar datos del Registro, una aplicación enumera normalmente las subclaves de una clave hasta que encuentra una determinada y, a continuación, recupera los datos del valor o los valores asociados a ella. Una aplicación puede llamar a [**la función RegEnumKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regenumkeyexa) para enumerar las subclaves de una clave determinada.

Para recuperar datos detallados sobre una subclave determinada, una aplicación puede llamar a la [**función RegQueryInfoKey.**](/windows/desktop/api/Winreg/nf-winreg-regqueryinfokeya) La [**función RegGetKeySecurity**](/windows/desktop/api/winreg/nf-winreg-reggetkeysecurity) recupera una copia del descriptor de seguridad que protege una clave.

Una aplicación puede usar la [**función RegEnumValue**](/windows/desktop/api/Winreg/nf-winreg-regenumvaluea) para enumerar los valores de una clave determinada y la función [**RegQueryValueEx**](/windows/desktop/api/Winreg/nf-winreg-regqueryvalueexa) para recuperar un valor determinado para una clave. Normalmente, una aplicación llama **a RegEnumValue para** determinar los nombres de valor y, a continuación, **RegQueryValueEx** para recuperar los datos de los nombres.

La [**función RegQueryMultipleValues**](/windows/desktop/api/Winreg/nf-winreg-regquerymultiplevaluesa) recupera el tipo y los datos de una lista de nombres de valor asociados a una clave del Registro abierta. Esta función es útil para los proveedores de claves dinámicas porque garantiza la coherencia de los datos mediante la recuperación de varios valores en una operación atómica.

Dado que otras aplicaciones pueden cambiar los datos de un valor del Registro entre el momento en que la aplicación puede leer un valor y usarlo, es posible que tenga que asegurarse de que la aplicación tiene los datos más recientes. Puede usar la función [**RegNotifyChangeKeyValue**](/windows/desktop/api/Winreg/nf-winreg-regnotifychangekeyvalue) para notificar al subproceso que realiza la llamada cuando haya cambios en los atributos o el contenido de una clave del Registro, o si se elimina la clave. La función señala un objeto de evento para notificar al autor de la llamada. Si se cierra el subproceso que llama a **RegNotifyChangeKeyValue,** se señala el evento y se detiene la supervisión de la clave del Registro.

Puede controlar o especificar qué cambios se deben notificar mediante el uso de un filtro o marca de notificación. Normalmente, los cambios se notifican mediante la señalización de un evento que se especifica en la función. Tenga en cuenta que [**la función RegNotifyChangeKeyValue**](/windows/desktop/api/Winreg/nf-winreg-regnotifychangekeyvalue) no funciona con identificadores remotos.

Para supervisar las operaciones del Registro con más detalle, vea [**Registro**](/windows/desktop/ETW/registry).

 

 
