---
description: Los evaluadores de coherencia internos, también denominados ICEs, son acciones personalizadas escritas en VBScript, JScript o como DLL o EXE.
ms.assetid: 0789103d-ae34-46be-a9fb-093e066d6d4b
title: Evaluadores de coherencia interna-CIEM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77be6e2bf33bbe348acab45191782a211ea4663a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688544"
---
# <a name="internal-consistency-evaluators---ices"></a>Evaluadores de coherencia interna-CIEM

Los evaluadores de coherencia internos, también denominados ICEs, son acciones personalizadas escritas en VBScript, JScript o como DLL o EXE. Cuando se ejecutan estas acciones personalizadas, examinan las entradas de los registros de la base de datos que son válidas cuando se examinan individualmente pero que pueden provocar un comportamiento incorrecto en el contexto de toda la base de datos. Tenga en cuenta que esto es diferente de la validación realizada en registros individuales mediante [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify).

Por ejemplo, la [tabla de componentes](component-table.md) puede mostrar varios componentes que son válidos cuando se prueban de forma individual con [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify). Sin embargo, **MsiViewModify** no detectaría el error cuando dos componentes usan el mismo [GUID](guid.md) que su código de componente. La acción personalizada [ICE08](ice08.md) está diseñada para validar que la tabla de componentes no contiene GUID de código de componente duplicados.

Las acciones personalizadas de ICE devuelven cuatro tipos de mensajes:

-   [**Errores**](merge-errors.md) de Mensajes de error creación de base de datos de informes que causan un comportamiento incorrecto. Por ejemplo, los GUID de componentes duplicados hacen que el instalador registre los componentes de forma incorrecta.
-   **Advertencias** Los mensajes de advertencia crean informes de creación de bases de datos que provocan un comportamiento incorrecto en ciertos casos. Las advertencias también pueden notificar efectos secundarios inesperados de la creación de bases de datos. Por ejemplo, al escribir el mismo nombre de propiedad en dos condiciones que solo difieren en el caso de las letras en el nombre. Dado que el instalador distingue entre mayúsculas y minúsculas, el instalador los trata como propiedades diferentes.
-   **Errores** de Los mensajes de error notifican el error de la acción personalizada ICE. El error se debe normalmente a una base de datos con problemas graves que el ICE no puede incluso ejecutar.
-   **Información** Los mensajes informativos proporcionan información del ICE y no indican ningún problema con la base de datos. A menudo, son información sobre el propio ICE, como una breve descripción. También pueden proporcionar información de progreso a medida que se ejecuta el hielo.

Para obtener más información, vea [usar evaluadores de coherencia interna](using-internal-consistency-evaluators.md).

 

 



