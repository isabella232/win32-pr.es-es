---
description: Sugerencias de diseño para desarrollar un CRM de COM+
ms.assetid: dde1b978-6d35-4a75-91fd-69dfcc6c43d2
title: Sugerencias de diseño para desarrollar un CRM de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a286b2aa75b266a41b249b29203b16f0441e6276a9de03a25efc622ac2bd3fdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128757"
---
# <a name="design-suggestions-for-developing-a-com-crm"></a>Sugerencias de diseño para desarrollar un CRM de COM+

A continuación se indican los pasos sugeridos para desarrollar un CRM de COM+:

1.  Antes de iniciar el desarrollo, establezca el tiempo de espera de la transacción en cero (mediante la herramienta administrativa Servicios de componentes). Establezca la marca del Registro VTRACE1 (vea [COM+ CRM Registry Configuración](com--crm-registry-settings.md)) para ver los mensajes de error y advertencia de CRM en el seguimiento de depuración.
2.  Determine qué conjunto de interfaces debe usar, estructurado (variantes) o no estructurado. (Vea [INTERFACES DE COM+ CRM).](com--crm-interfaces.md) Esto dependerá del lenguaje que use para desarrollar crm, por ejemplo, Microsoft Visual C++ o Microsoft Visual Basic.
3.  Desarrolle primero el trabajo de CRM. Determine la información necesaria en las entradas de registro. Defina los tipos de registros necesarios y su formato.
4.  Se proporciona un compensador CRM de depuración como parte de los ejemplos de CRM (en Windows SDK). Esto se puede usar temporalmente al depurar el trabajo de CRM en lugar del compensador de CRM real.
5.  Cuando el trabajo de CRM funcione correctamente, desarrolle el compensador crm real y reemplace el compensador crm de depuración por el compensador crm real.
6.  Puede ser conveniente no probar inicialmente el caso de recuperación. Si es así, elimine el archivo de registro de CRM para la aplicación de servidor CRM cada vez antes de iniciar esa aplicación de servidor CRM.

## <a name="considerations"></a>Consideraciones

1.  **Escriba con antelación.** El componente de trabajo de CRM debe escribir con antelación; es decir, debe escribir una entrada de registro que indique que va a realizar una acción antes de realizar realmente esa acción. Además, esta entrada de registro debe forzarse en el disco después de la escritura y antes de realizar la acción.
2.  **Aislamiento.** CRM no aplica el aislamiento. El diseño de CRM debe proporcionar aislamiento entre varios clientes en transacciones independientes y también debe tener en cuenta el caso antes de la recuperación.
3.  **Recuperación en curso.** El trabajo de CRM debe controlar el código de error "recuperación en curso". Consulte [Solución de problemas de COM+ CRM](troubleshooting-the-com--crm.md) para obtener más información sobre este código de error.
4.  **Control de errores.** El trabajo de CRM debe hacer frente al caso en el que la transacción se anula antes de lo esperado. Consulte la sección [Control de errores en COM+ CRM.](error-handling-in-the-com--crm.md)
5.  **Tiempo de recuperación.** El compensador CRM debe diseñarse para realizar la recuperación rápidamente de modo que el nuevo trabajo para esa aplicación de servidor CRM no tenga que esperar.
6.  **Idempotence.** Es posible que un compensador de CRM vuelva a recibir la misma entrada de registro para deshacer o rehacer una acción que ya se ha deshacido o rehacer. Las acciones que podría realizar el compensador de CRM deben ser idempotentes, lo que a menudo significa que se deben omitir los códigos de error devueltos por estas acciones.
7.  **Iniciación de la recuperación.** La recuperación de una aplicación de servidor CRM se realiza cuando se inicia esa aplicación de servidor CRM. Sin embargo, no hay ningún inicio automático de una aplicación de servidor CRM. El desarrollador de la aplicación debe tener en cuenta cómo se deben iniciar el inicio y la recuperación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos de compensación Resource Manager COM+](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



