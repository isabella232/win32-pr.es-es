---
description: Los controladores de superposición de iconos son objetos del Modelo de objetos componentes (COM) en proceso, implementados como archivos DLL.
ms.assetid: ADF27BFD-CC96-43F9-9EBB-DEBE0DEA7B92
title: Cómo implementar controladores de superposición de iconos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8745d0d5c0cf9c69f28f0235ecc82acb07a14f1e3408d7fa7d65cf729e01403f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117859702"
---
# <a name="how-to-implement-icon-overlay-handlers"></a>Cómo implementar controladores de superposición de iconos

Los controladores de superposición de iconos son objetos del Modelo de objetos componentes (COM) en proceso, implementados como archivos DLL. Exportan una interfaz además de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**IShellIconOverlayIdentifier.**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelliconoverlayidentifier) Esta interfaz tiene tres métodos: [**IShellIconOverlayIdentifier::GetOverlayInfo**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getoverlayinfo), [**IShellIconOverlayIdentifier::GetPriority**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getpriority)e [**IShellIconOverlayIdentifier::IsMemberOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-ismemberof).

## <a name="instructions"></a>Instructions

### <a name="step-1-implementing-getoverlayinfo"></a>Paso 1: Implementar GetOverlayInfo

Se [**llama primero al método GetOverlayInfo**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getoverlayinfo) durante la inicialización. El método devuelve la ruta de acceso completa del archivo que contiene la imagen de superposición de iconos y su índice de base cero dentro del archivo. A continuación, el shell agrega la imagen a la lista de imágenes del sistema. Las superposiciones de iconos se pueden incluir en cualquiera de los tipos de archivo estándar, incluidos .exe, .dll y .ico.

Una vez completada la inicialización, el Shell llama a [**GetOverlayInfo**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getoverlayinfo) cuando necesita mostrar la superposición de iconos del controlador. El método debe devolver el mismo nombre de archivo e índice que hizo durante la inicialización. Aunque el Shell usa la imagen almacenada en caché en la lista de imágenes del sistema en lugar de cargar la imagen desde el archivo, todavía se identifica una superposición de iconos por su nombre de archivo y su índice.

### <a name="step-2-implementing-getpriority"></a>Paso 2: Implementar GetPriority

Solo [**se llama al método GetPriority**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getpriority) durante la inicialización. Asigna un valor de prioridad a la superposición de iconos del controlador. El valor puede oscilar entre cero y 100, donde 100 es la prioridad más baja. El propósito de este valor de prioridad es ayudar al Shell a resolver el conflicto que surge cuando se especifican varias superposiciones de iconos para un solo objeto. El Shell usa primero un conjunto interno de reglas para determinar la superposición de iconos de prioridad más alta. Si estas reglas no resuelven el conflicto, los valores asignados a las superposiciones de icono por **GetPriority** determinan la prioridad.

El valor de prioridad establecido por [**GetPriority**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getpriority) no es una manera confiable de resolver conflictos entre controladores de superposición de iconos no relacionados. No hay ninguna manera de que el controlador determine qué valores de prioridad usan otros controladores. Normalmente, debe establecer el valor en cero. Sin embargo, el valor de prioridad es útil cuando se han implementado dos o más controladores de superposición de iconos que pueden solicitar iconos de superposición de iconos para el mismo objeto. Si establece los valores de prioridad correctamente, puede especificar cuál de las superposiciones de icono solicitadas se mostrará.

### <a name="step-3-implementing-ismemberof"></a>Paso 3: Implementar IsMemberOf

El Shell llama al [**método IsMemberOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-ismemberof) para determinar si debe mostrar la superposición de iconos de un controlador para un objeto determinado. El shell especifica el objeto pasando su nombre al método . Si un controlador quiere que se muestre su superposición de iconos, **IsMemberOf** devuelve S \_ OK. Si no es así, devuelve S \_ FALSE.

Los controladores de superposición de iconos están diseñados normalmente para funcionar con un grupo determinado de archivos. Un ejemplo típico es un [tipo de archivo](fa-file-types.md), identificado por una extensión de nombre de archivo específica. Un controlador de superposición de iconos puede solicitar una superposición de iconos para todos los archivos del tipo de archivo. Algunos controladores solicitan una superposición de iconos solo si un archivo del tipo de archivo está en un estado determinado. Sin embargo, los controladores de superposición de iconos pueden solicitar su superposición de iconos para cualquier objeto que elijan.

 

 
