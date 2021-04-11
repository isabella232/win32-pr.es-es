---
description: Sugerencias de diseño para desarrollar un CRM de COM+
ms.assetid: dde1b978-6d35-4a75-91fd-69dfcc6c43d2
title: Sugerencias de diseño para desarrollar un CRM de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dcdb59f0ea23fb6879300d0bacec7df12970d81
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274950"
---
# <a name="design-suggestions-for-developing-a-com-crm"></a>Sugerencias de diseño para desarrollar un CRM de COM+

A continuación se indican los pasos sugeridos para desarrollar un CRM de COM+:

1.  Antes de comenzar el desarrollo, establezca el tiempo de espera de la transacción en cero (mediante la herramienta administrativa Servicios de componentes). Establezca la marca del registro VTRACE1 (consulte [configuración del registro de com+ CRM](com--crm-registry-settings.md)) para ver los mensajes de error y de advertencia de CRM en el seguimiento de depuración.
2.  Determine el conjunto de interfaces que necesita usar, estructurado (Variant) o no estructurado. (Consulte [interfaces de com+ CRM](com--crm-interfaces.md)). Esto dependerá del idioma que use para desarrollar su CRM, por ejemplo, Microsoft Visual C++ o Microsoft Visual Basic.
3.  Desarrolle primero el trabajador de CRM. Determine la información necesaria en las entradas de registro. Defina los tipos de entradas de registro necesarias y su formato.
4.  Un compensador de CRM de depuración se proporciona como parte de los ejemplos de CRM (en el Windows SDK). Se puede usar temporalmente al depurar el trabajo de CRM en lugar del compensador real de CRM.
5.  Cuando el trabajo de CRM funcione correctamente, desarrolle el compensador de CRM real y reemplace el compensador de depuración de CRM por el compensador real de CRM.
6.  Puede ser conveniente no probar inicialmente el caso de recuperación. En ese caso, elimine el archivo de registro de CRM de la aplicación de servidor CRM cada vez antes de iniciar la aplicación de servidor CRM.

## <a name="considerations"></a>Consideraciones

1.  **Escritura previa.** El componente de trabajo de CRM debe escribir de antemano; es decir, debe escribir una entrada de registro que indique que va a realizar una acción antes de realizar esa acción. Además, esta entrada de registro se debe forzar al disco después de la escritura y antes de que se realice la acción.
2.  **Aislamiento.** CRM no aplica el aislamiento. El diseño de CRM debe proporcionar aislamiento entre varios clientes en transacciones independientes y también debe tener en cuenta las mayúsculas y minúsculas antes de la recuperación.
3.  **Recuperación en curso.** El trabajador de CRM debe controlar el código de error "recuperación en curso". Consulte [solución de problemas de com+ CRM](troubleshooting-the-com--crm.md) para obtener más información sobre este código de error.
4.  **Control de errores.** El trabajo de CRM debe hacer frente al caso en el que la transacción se anula antes de lo esperado. Vea la sección [control de errores en el CRM de com+](error-handling-in-the-com--crm.md).
5.  **Tiempo de recuperación.** El compensador de CRM debe estar diseñado para realizar la recuperación rápidamente, de modo que el nuevo trabajo para esa aplicación de CRM Server no tenga que esperar.
6.  **Idempotencia.** Es posible que un compensador de CRM vuelva a recibir el mismo registro de registro para deshacer o rehacer una acción que ya se ha deshecho o rehecho. Las acciones que el compensador de CRM podría realizar deben ser idempotente, lo que a menudo significa que se deben omitir los códigos de error devueltos por estas acciones.
7.  **Inicio de la recuperación.** La recuperación de una aplicación de servidor CRM se realiza cuando se inicia la aplicación de servidor CRM. Sin embargo, no hay ningún Inicio automático de una aplicación de servidor CRM. El desarrollador de la aplicación debe considerar cómo debe iniciarse el inicio y la recuperación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos de Administrador de recursos de compensación de COM+](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



