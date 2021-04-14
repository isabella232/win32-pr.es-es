---
description: Control de errores en COM+ CRM
ms.assetid: 9de31fb5-31e9-494a-b61f-87bcff0d5085
title: Control de errores en COM+ CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aba2b5c4541485433a85fe01fee7870c2e43f62
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496342"
---
# <a name="error-handling-in-the-com-crm"></a>Control de errores en COM+ CRM

Las aplicaciones de servidor COM+ implementan una directiva FailFast. Si se detecta un error interno grave, el proceso de aplicación de servidor se cierra y escribe un mensaje de error en el registro de eventos de Windows. Esto permite la detección rápida de problemas y es posible debido a la protección de los datos de la aplicación por el procesamiento de transacciones. Compruebe siempre el registro de eventos de Windows en busca de errores de CRM, ya sea durante el desarrollo o durante la implementación final.

Errores básicos en el uso de las interfaces de CRM, como argumentos no válidos o errores de secuencia (por ejemplo, si se intenta escribir una entrada de registro antes de registrar el compensador de CRM), devuelven códigos de error y no deben desencadenar FailFast. Para el desarrollo de CRM, puede optar por establecer la clave del registro VTRACE1 (consulte [configuración del registro de com+ CRM](com--crm-registry-settings.md)), que hace que aparezca un mensaje en la ventana de salida del depurador para cada error.

También se pueden producir errores transitorios. Normalmente, estos errores se deben a condiciones de control de tiempo y provocan que se devuelva un código de error. El desarrollador de CRM debe asegurarse de que se controlen estas condiciones de error. Por ejemplo, al escribir una entrada de registro, la transacción podría anularse debido a un tiempo de espera. Después, el método devuelve un error, que el autor de la llamada debe comprobar y controlar de forma adecuada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos de Administrador de recursos de compensación de COM+](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



