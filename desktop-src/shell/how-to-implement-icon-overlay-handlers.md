---
description: Los controladores de superposición de iconos son objetos de modelo de objetos componentes (COM) en proceso, implementados como archivos dll.
ms.assetid: ADF27BFD-CC96-43F9-9EBB-DEBE0DEA7B92
title: Cómo implementar controladores de superposición de iconos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e22c1057f65c50b31c6627846ec77103827a0283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985427"
---
# <a name="how-to-implement-icon-overlay-handlers"></a>Cómo implementar controladores de superposición de iconos

Los controladores de superposición de iconos son objetos de modelo de objetos componentes (COM) en proceso, implementados como archivos dll. Exportan una interfaz además de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**IShellIconOverlayIdentifier**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelliconoverlayidentifier). Esta interfaz tiene tres métodos: [**IShellIconOverlayIdentifier:: GetOverlayInfo**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getoverlayinfo), [**IShellIconOverlayIdentifier:: GetPriority (**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getpriority)y [**IShellIconOverlayIdentifier:: IsMemberOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-ismemberof).

## <a name="instructions"></a>Instrucciones

### <a name="step-1-implementing-getoverlayinfo"></a>Paso 1: implementación de GetOverlayInfo

Primero se llama al método [**GetOverlayInfo**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getoverlayinfo) durante la inicialización. El método devuelve la ruta de acceso completa del archivo que contiene la imagen de superposición de icono y su índice de base cero dentro del archivo. Después, el shell agrega la imagen a la lista de imágenes del sistema. Las superposiciones de iconos pueden estar contenidas en cualquiera de los tipos de archivo estándar, como. exe,. dll y. ico.

Una vez completada la inicialización, el shell llama a [**GetOverlayInfo**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getoverlayinfo) cuando necesita mostrar la superposición de iconos del controlador. El método debe devolver el mismo nombre de archivo y el mismo índice que tenía durante la inicialización. Aunque el shell usa la imagen que está almacenada en la memoria caché en la lista de imágenes del sistema en lugar de cargar la imagen desde el archivo, una superposición de iconos sigue siendo identificada por su nombre de archivo e índice.

### <a name="step-2-implementing-getpriority"></a>Paso 2: implementación de GetPriority (

Solo se llama al método [**GetPriority (**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getpriority) durante la inicialización. Asigna un valor de prioridad a la superposición de iconos del controlador. El valor puede oscilar entre cero y 100, donde 100 es la prioridad más baja. El propósito de este valor de prioridad es ayudar a que el shell resuelva el conflicto que surge cuando se especifican varias superposiciones de iconos para un único objeto. El shell usa primero un conjunto interno de reglas para determinar la superposición del icono de prioridad más alta. Si estas reglas no resuelven el conflicto, los valores asignados al icono superpuesto de **GetPriority (** determinan la prioridad.

El valor de prioridad establecido por [**GetPriority (**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getpriority) no es una manera confiable de resolver conflictos entre controladores de superposición de iconos no relacionados. No hay ninguna manera de que el controlador determine qué valores de prioridad usan otros controladores. Normalmente, el valor se debe establecer en cero. Sin embargo, el valor de prioridad es útil cuando se han implementado dos o más controladores de superposición de iconos que pueden solicitar iconos de superposición de iconos para el mismo objeto. Al establecer los valores de prioridad adecuadamente, puede especificar cuál de las superposiciones de iconos solicitadas se mostrará.

### <a name="step-3-implementing-ismemberof"></a>Paso 3: implementación de IsMemberOf

El shell llama al método [**IsMemberOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-ismemberof) para determinar si debe mostrar la superposición de icono de un controlador para un objeto determinado. El shell especifica el objeto pasando su nombre al método. Si un controlador desea mostrar su superposición de icono, **IsMemberOf** devuelve S \_ correcto. Si no es así, devuelve S \_ false.

Los controladores de superposición de iconos suelen estar diseñados para trabajar con un grupo de archivos determinado. Un ejemplo típico es un [tipo de archivo](fa-file-types.md), identificado por una extensión de nombre de archivo específica. Un controlador de superposición de iconos puede solicitar una superposición de iconos para todos los archivos del tipo de archivo. Algunos controladores solicitan una superposición de iconos solo si un archivo del tipo de archivo se encuentra en un estado determinado. Sin embargo, los controladores de superposición de iconos pueden solicitar la superposición de iconos para cualquier objeto que elijan.

 

 
