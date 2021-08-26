---
title: Restaurar sistema
description: Establece los puntos de restauración del sistema y supervisa los cambios clave del sistema de un programa para habilitar una reversión del sistema a un estado anterior. Escriba código de recuperación automática o script wmi para restaurar el estado del sistema en un punto de restauración registrado.
ms.assetid: 6861eedc-2bd9-49c7-8682-ea557fa29d28
keywords:
- Restaurar sistema
- Restaurar sistema, página de inicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4472806aa2c0b6f8a29cc4e687d16e262639a66c65bda37fdca970c6c38b656f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111295"
---
# <a name="system-restore"></a>Restaurar sistema

## <a name="purpose"></a>Propósito

Restaurar sistema supervisa y registra automáticamente los cambios clave del sistema en el equipo de un usuario. Está diseñado para reducir los costos de soporte técnico y aumentar la satisfacción del cliente al permitir a un usuario deshacer un cambio que puede haber causado un problema con el sistema o revertir a un día en el que el sistema funcionaba de forma óptima.

> [!Note]  
> La siguiente documentación está dirigida a desarrolladores. Si es un usuario final que busca información sobre cómo usar Restaurar sistema, consulte [¿Qué es Restaurar sistema?](https://windows.microsoft.com/windows/What-is-System-Restore#1TC=windows-7)

 

## <a name="developer-audience"></a>Audiencia de desarrolladores

La API Restaurar sistema está diseñada para su uso por los programadores de C/C++. Es necesario estar familiarizado con Windows Management Instrumentation (WMI) para usar la interfaz de scripting.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

La API Restaurar sistema se admite en sistemas operativos cliente a partir de Windows XP. Para obtener información sobre qué sistemas operativos deben usar un elemento de API determinado, consulte la sección Requisitos de su documentación.

## <a name="in-this-section"></a>En esta sección



| Tema                                                | Descripción                                                                    |
|------------------------------------------------------|--------------------------------------------------------------------------------|
| [Información general](about-system-restore.md)<br/>      | Información general sobre cómo Restaurar sistema trabajo.<br/>                            |
| [Referencia](system-restore-reference.md)<br/> | Documentación de Restaurar sistema, estructuras y clases.<br/> |
| [Ejemplos](using-system-restore.md)<br/>       | Un programa de ejemplo escrito en C.<br/>                                      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[WMI](/windows/desktop/WmiSdk/wmi-start-page)
</dt> </dl>

 

