---
description: El instalador escribe los siguientes valores en el registro cuando una acción devuelve estos códigos de error. Para obtener la lista completa de códigos de error devueltos por la función Windows installer MsiExec.exe y InstMsi.exe, vea Códigos de error.
ms.assetid: 653bbf45-ac2c-4f8a-a978-960e0c42e6e4
title: Registro de valores devueltos de acción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaaa203fee1fbb02bef070d065a9838383ea588b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074423"
---
# <a name="logging-of-action-return-values"></a>Registro de valores devueltos de acción

El instalador escribe los siguientes valores en el registro cuando una acción devuelve estos códigos de error. Para obtener la lista completa de códigos de error devueltos por la función Windows Installer MsiExec.exe y InstMsi.exe, vea [Códigos de error](error-codes.md).



| Código de error                       | Valores devueltos por llamadas de función MsiExec.exe y InstMsi.exe | Valores que aparecen en el registro. | Descripción                                                                                                                                                                                                                                                                     |
|----------------------------------|----------------------------------------------------------------|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FUNCIÓN DE \_ ERROR \_ NO \_ LLAMADA     | 1626                                                           | 0                              | No se pudo ejecutar una función.                                                                                                                                                                                                                                               |
| ERROR \_ CORRECTO                   | 0                                                              | 1                              | Una acción completada correctamente.                                                                                                                                                                                                                                               |
| ERROR \_ AL \_ INSTALAR USEREXIT         | 1602                                                           | 2                              | Un usuario canceló la instalación.                                                                                                                                                                                                                                                   |
| ERROR DE \_ INSTALACIÓN \_          | 1603                                                           | 3                              | Un error irresal.                                                                                                                                                                                                                                                                  |
| ERROR \_ INSTALL \_ SUSPEND          | 1604                                                           | 4                              | La instalación está suspendida, incompleta.                                                                                                                                                                                                                                         |
| ERROR \_ CORRECTO                   | 0                                                              | 5                              | La acción se completó correctamente.                                                                                                                                                                                                                                              |
| ERROR \_ ESTADO DE IDENTIFICADOR NO \_ \_ VÁLIDO    | 1609                                                           | 6                              | El identificador está en un estado no válido.                                                                                                                                                                                                                                              |
| ERROR \_ DATOS NO \_ VÁLIDOS             | 1626                                                           | 7                              | Los datos no son válidos.                                                                                                                                                                                                                                                            |
| ERROR \_ AL INSTALAR YA EN \_ \_ EJECUCIÓN | 1618                                                           | 8                              | Hay otra instalación en curso. Solo una instalación a la vez puede ejecutar acciones en las tablas [InstallExecuteSequence,](installexecutesequence-table.md) [AdminExecuteSequence](adminexecutesequence-table.md)o [AdvtExecuteSequence.](advtexecutesequence-table.md) |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Registro del instalador](windows-installer-logging.md)
</dt> </dl>

 

 



