---
description: Control de errores en COM+ CRM
ms.assetid: 9de31fb5-31e9-494a-b61f-87bcff0d5085
title: Control de errores en COM+ CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aba2b5c4541485433a85fe01fee7870c2e43f62
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465687"
---
# <a name="error-handling-in-the-com-crm"></a>Control de errores en COM+ CRM

Las aplicaciones de servidor COM+ implementan una directiva de error. Si se detecta un error interno grave, el proceso de aplicación de servidor se cierra y escribe un mensaje de error en el Windows de eventos. Esto permite la detección rápida de problemas y es posible debido a la protección de los datos de la aplicación mediante el procesamiento de transacciones. Compruebe siempre el Windows de eventos para ver si hay errores del CRM, ya sea durante el desarrollo o durante la implementación final.

Errores básicos al usar las interfaces crm, como argumentos no válidos o errores de secuencia (por ejemplo, intentar escribir una entrada de registro antes de registrar el compensador de CRM), devolver códigos de error y no debe desencadenar failfast. Para el desarrollo de CRM, puede optar por establecer la clave del Registro VTRACE1 (vea [COM+ CRM Registry Configuración](com--crm-registry-settings.md)), lo que hace que aparezca un mensaje en la ventana de salida del depurador para cada error.

También se pueden producir errores transitorios. Estos errores suelen deberse a condiciones de control de tiempo y producen un código de error que se devuelve. El desarrollador de CRM debe asegurarse de que se controlan estas condiciones de error. Por ejemplo, al escribir una entrada de registro, la transacción podría anularse debido a un tiempo de espera. A continuación, el método devuelve un error que el autor de la llamada debe comprobar y controlar correctamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos de compensación Resource Manager COM+](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



