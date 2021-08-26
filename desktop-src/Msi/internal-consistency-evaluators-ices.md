---
description: Los evaluadores de coherencia internos, también denominados CIE, son acciones personalizadas escritas en VBScript, JScript o como un archivo DLL o EXE.
ms.assetid: 0789103d-ae34-46be-a9fb-093e066d6d4b
title: 'Evaluadores de coherencia internos: TIC'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 744915d7f484128095e308f390caae75323775b684b38a0184592dc99a2700f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043385"
---
# <a name="internal-consistency-evaluators---ices"></a>Evaluadores de coherencia internos: TIC

Los evaluadores de coherencia internos, también denominados CIE, son acciones personalizadas escritas en VBScript, JScript o como un archivo DLL o EXE. Cuando se ejecutan estas acciones personalizadas, examinan la base de datos en busca de entradas en los registros de base de datos que son válidas cuando se examinan individualmente, pero que pueden provocar un comportamiento incorrecto en el contexto de toda la base de datos. Tenga en cuenta que esto es diferente de la validación realizada en registros individuales [**mediante MsiViewModify.**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify)

Por ejemplo, la [tabla Component puede](component-table.md) enumerar varios componentes que son válidos cuando se prueban individualmente con [**MsiViewModify.**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) Sin embargo, **MsiViewModify** no detectaría el error cuando dos componentes usan el mismo [GUID](guid.md) que su código de componente. La acción personalizada [ICE08](ice08.md) está diseñada para validar que la tabla Component no contiene GUID de código de componente duplicados.

Las acciones personalizadas de ICE devuelven cuatro tipos de mensajes:

-   [**Errores**](merge-errors.md) Los mensajes de error informan de la creación de bases de datos que provocan un comportamiento incorrecto. Por ejemplo, los GUID de componentes duplicados hacen que el instalador registre incorrectamente los componentes.
-   **Advertencias** Los mensajes de advertencia informan de la creación de la base de datos que provoca un comportamiento incorrecto en determinados casos. Las advertencias también pueden notificar efectos secundarios inesperados de la creación de bases de datos. Por ejemplo, escribir el mismo nombre de propiedad en dos condiciones que solo difieren en el caso de las letras del nombre. Dado que el instalador distingue mayúsculas de minúsculas, los trata como propiedades diferentes.
-   **Errores** Los mensajes de error informan del error de la acción personalizada de ICE. El error se debe normalmente a una base de datos con problemas tan graves que el ICE ni siquiera puede ejecutarse.
-   **Informativo** Los mensajes informativos proporcionan información del ICE y no indican un problema con la base de datos. A menudo son información sobre el propio ICE, como una breve descripción. También pueden proporcionar información de progreso a medida que se ejecuta el ICE.

Para obtener más información, [vea Using Internal Consistency Evaluators](using-internal-consistency-evaluators.md).

 

 



