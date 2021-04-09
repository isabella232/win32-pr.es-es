---
title: Restaurar sistema
description: Establece los puntos de restauración del sistema y supervisa los cambios del sistema de claves de un programa para permitir la reversión del sistema a un estado anterior. Escriba el código de recuperación automática o el script de WMI para restaurar el estado del sistema en un punto de restauración registrado.
ms.assetid: 6861eedc-2bd9-49c7-8682-ea557fa29d28
keywords:
- Restaurar sistema
- Restaurar sistema, página de inicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e0bdc4555171ad867f6e6b925144d9ed673ffc3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149420"
---
# <a name="system-restore"></a>Restaurar sistema

## <a name="purpose"></a>Propósito

Restaurar sistema supervisa y registra automáticamente los cambios del sistema de claves en el equipo de un usuario. Está diseñado para reducir los costos de soporte técnico y aumentar la satisfacción del cliente al permitir que un usuario deshaga un cambio que puede haber causado un problema en el sistema o revertir a un día en el que el sistema funcionaba de forma óptima.

> [!Note]  
> La siguiente documentación está dirigida a los desarrolladores. Si es un usuario final que busca información sobre cómo usar Restaurar sistema, consulte [¿Qué es restaurar sistema?](https://windows.microsoft.com/windows/What-is-System-Restore#1TC=windows-7)

 

## <a name="developer-audience"></a>Audiencia de desarrolladores

La API de restauración del sistema está diseñada para que la usen los programadores de C/C++. Es necesario estar familiarizado con Instrumental de administración de Windows (WMI) para usar la interfaz de scripting.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

La API de restauración del sistema se admite en sistemas operativos de cliente a partir de Windows XP. Para obtener información sobre los sistemas operativos necesarios para usar un elemento de API determinado, consulte la sección de requisitos de la documentación.

## <a name="in-this-section"></a>En esta sección



| Tema                                                | Descripción                                                                    |
|------------------------------------------------------|--------------------------------------------------------------------------------|
| [Información general](about-system-restore.md)<br/>      | Información general sobre cómo funciona la restauración del sistema.<br/>                            |
| [Referencia](system-restore-reference.md)<br/> | Documentación de las funciones, estructuras y clases de restaurar sistema.<br/> |
| [Ejemplos](using-system-restore.md)<br/>       | Programa de ejemplo escrito en C.<br/>                                      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[WMI](/windows/desktop/WmiSdk/wmi-start-page)
</dt> </dl>

 

