---
description: El instalador escribe los siguientes valores en el registro cuando una acción devuelve estos códigos de error. Para obtener la lista completa de los códigos de error devueltos por la función Windows Installer llama a MsiExec.exe y InstMsi.exe, vea códigos de error.
ms.assetid: 653bbf45-ac2c-4f8a-a978-960e0c42e6e4
title: Registro de valores devueltos de acción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaaa203fee1fbb02bef070d065a9838383ea588b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688638"
---
# <a name="logging-of-action-return-values"></a>Registro de valores devueltos de acción

El instalador escribe los siguientes valores en el registro cuando una acción devuelve estos códigos de error. Para obtener la lista completa de los códigos de error devueltos por la función Windows Installer llama a MsiExec.exe y InstMsi.exe, vea [códigos de error](error-codes.md).



| Código de error                       | Los valores devueltos por las llamadas de función MsiExec.exe y InstMsi.exe | Valores que aparecen en el registro. | Descripción                                                                                                                                                                                                                                                                     |
|----------------------------------|----------------------------------------------------------------|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| función de ERROR \_ \_ no \_ llamada     | 1626                                                           | 0                              | No se pudo ejecutar una función.                                                                                                                                                                                                                                               |
| ERROR \_ correcto                   | 0                                                              | 1                              | Una acción se completó correctamente.                                                                                                                                                                                                                                               |
| ERROR al \_ instalar \_ USEREXIT         | 1602                                                           | 2                              | Un usuario canceló la instalación.                                                                                                                                                                                                                                                   |
| ERROR de instalación de ERROR \_ \_          | 1603                                                           | 3                              | Error irrecuperable.                                                                                                                                                                                                                                                                  |
| ERROR de \_ instalación de \_ suspensión          | 1604                                                           | 4                              | La instalación se suspendió, está incompleta.                                                                                                                                                                                                                                         |
| ERROR \_ correcto                   | 0                                                              | 5                              | La acción se completó correctamente.                                                                                                                                                                                                                                              |
| ERROR \_ de \_ Estado de identificador no válido \_    | 1609                                                           | 6                              | El identificador está en un estado no válido.                                                                                                                                                                                                                                              |
| ERROR de \_ datos no válidos \_             | 1626                                                           | 7                              | Los datos no son válidos.                                                                                                                                                                                                                                                            |
| la \_ instalación de error \_ ya se \_ está ejecutando | 1618                                                           | 8                              | Hay otra instalación en curso. Solo una instalación a la vez puede ejecutar acciones en las tablas [InstallExecuteSequence](installexecutesequence-table.md), [AdminExecuteSequence](adminexecutesequence-table.md)o [AdvtExecuteSequence](advtexecutesequence-table.md) . |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registro de Windows Installer](windows-installer-logging.md)
</dt> </dl>

 

 



