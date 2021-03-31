---
description: Un directorio que contiene uno o varios directorios es el elemento primario del directorio o directorios contenidos y cada directorio contenido es un elemento secundario del directorio principal. La estructura jerárquica de los directorios se conoce como un árbol de directorios.
ms.assetid: e8a7bf82-0f3c-4ad9-9d10-25c4d69733dc
title: Acerca de la administración de directorios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e3a90b6cc99a480f798e632512770c904291a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907995"
---
# <a name="about-directory-management"></a>Acerca de la administración de directorios

Un directorio que contiene uno o varios directorios es el *elemento primario* del directorio o directorios contenidos y cada directorio contenido es un *elemento secundario* del directorio principal. La estructura jerárquica de los directorios se conoce como un *árbol de directorios*.

El sistema de archivos NTFS implementa el vínculo lógico entre un directorio y los archivos que contiene como una *tabla de entradas de directorio*. Cuando se mueve un archivo a un directorio, se crea una entrada en la tabla para el archivo que se ha cambiado y el nombre del archivo se coloca en la entrada. Cuando se elimina un archivo contenido en un directorio, el nombre y la entrada correspondientes al archivo eliminado también se eliminan de la tabla. Puede haber más de una entrada para un único archivo en una tabla de entradas de directorio. Si se crea una entrada adicional en la tabla para un archivo, se hace referencia a esa entrada como un *vínculo físico* a ese archivo. No hay ningún límite en el número de vínculos físicos que se pueden crear para un único archivo.

Los directorios también pueden contener uniones y puntos de reanálisis.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                 | Descripción                                                                                            |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Crear y eliminar directorios](creating-and-deleting-directories.md)<br/> | Una aplicación puede crear y eliminar directorios mediante programación.<br/>                          |
| [Identificadores de directorio](obtaining-a-handle-to-a-directory.md)<br/>                 | Cada vez que un proceso crea o abre un objeto de directorio, recibe un identificador para el objeto.<br/> |
| [Puntos de análisis](reparse-points.md)<br/>                                       | Describe los puntos de reanálisis.<br/>                                                                   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de administración de directorios](directory-management-reference.md)
</dt> </dl>

 

 




