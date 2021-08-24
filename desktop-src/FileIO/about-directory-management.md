---
description: Un directorio que contiene uno o varios directorios es el elemento primario del directorio o directorios contenidos, y cada directorio contenido es un elemento secundario del directorio primario. La estructura jerárquica de directorios se conoce como árbol de directorios.
ms.assetid: e8a7bf82-0f3c-4ad9-9d10-25c4d69733dc
title: Acerca de la administración de directorios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9cc59e465e1d97b28b1cfdff35c5f288e56b5eb0ee9800273873ffe6476868b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766415"
---
# <a name="about-directory-management"></a>Acerca de la administración de directorios

Un directorio que contiene uno o  varios directorios es el elemento primario del directorio  o directorios contenidos, y cada directorio contenido es un elemento secundario del directorio primario. La estructura jerárquica de directorios se conoce como un árbol *de directorios*.

El sistema de archivos NTFS implementa el vínculo lógico entre un directorio y los archivos que contiene como una tabla *de entrada de directorio*. Cuando se mueve un archivo a un directorio, se crea una entrada en la tabla para el archivo movido y el nombre del archivo se coloca en la entrada. Cuando se elimina un archivo contenido en un directorio, el nombre y la entrada correspondientes al archivo eliminado también se eliminan de la tabla. Puede haber más de una entrada para un único archivo en una tabla de entrada de directorio. Si se crea una entrada adicional en la tabla para un archivo, esa entrada se conoce como un *vínculo duro* a ese archivo. No hay ningún límite en el número de vínculos duros que se pueden crear para un único archivo.

Los directorios también pueden contener uniones y puntos de rean aproximado.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                 | Descripción                                                                                            |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Creación y eliminación de directorios](creating-and-deleting-directories.md)<br/> | Una aplicación puede crear y eliminar directorios mediante programación.<br/>                          |
| [Identificadores de directorio](obtaining-a-handle-to-a-directory.md)<br/>                 | Cada vez que un proceso crea o abre un objeto de directorio, recibe un identificador para el objeto .<br/> |
| [Puntos de análisis](reparse-points.md)<br/>                                       | Describe los puntos de reanción.<br/>                                                                   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de administración de directorios](directory-management-reference.md)
</dt> </dl>

 

 




