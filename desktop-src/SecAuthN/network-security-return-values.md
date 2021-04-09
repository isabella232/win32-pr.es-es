---
description: Valores devueltos que puede establecer un proveedor de red.
ms.assetid: f8e6692f-4824-40fe-a5b3-9843689ea02e
title: Valores devueltos de seguridad de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a362fde712d2a44565894aceb9d85172e488b53a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002549"
---
# <a name="network-security-return-values"></a>Valores devueltos de seguridad de red

Los valores devueltos que puede establecer un proveedor de red incluyen los siguientes códigos de error.



| Códigos de error         | Descripción                                                                                                                                                                                                                                                                                                                             |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WN \_ correcto         | La función se ha realizado correctamente.                                                                                                                                                                                                                                                                                                                 |
| WN \_ no \_ compatible  | La función no se admite en este proveedor de red.                                                                                                                                                                                                                                                                                 |
| \_error de red WN \_      | Se ha producido un error de red desconocido.                                                                                                                                                                                                                                                                                                       |
| WN \_ más \_ datos      | El búfer de datos pasado no es suficiente para contener todos los datos disponibles.                                                                                                                                                                                                                                                         |
| WN \_ ( \_ puntero incorrecto)    | Se especificó un puntero no válido durante la llamada de función.                                                                                                                                                                                                                                                                     |
| WN \_ \_ valor incorrecto      | Se especificó un valor numérico no válido durante la llamada de función.                                                                                                                                                                                                                                                               |
| WN \_ \_ contraseña incorrecta   | Se especificó una contraseña incorrecta.                                                                                                                                                                                                                                                                                                    |
| WN \_ acceso \_ denegado  | El autor de la llamada no tiene permisos suficientes para completar la operación.                                                                                                                                                                                                                                                              |
| \_función WN \_ busy  | Esta función no se puede volver a escribir y se está usando actualmente, o bien el proveedor todavía se está inicializando y aún no está listo para ser llamado. El proveedor debe devolver este código de error solo si va a estar disponible. El MPR pasa este código de retorno a su llamador y es probable que haga que el llamador vuelva a intentarlo.<br/> |
| \_error de Windows WN \_  | Error en una función necesaria.                                                                                                                                                                                                                                                                                                             |
| WN \_ \_ usuario incorrecto       | Se especificó un nombre de usuario no válido.                                                                                                                                                                                                                                                                                            |
| WN \_ \_ memoria insuficiente \_ | No hay memoria suficiente para completar la operación.                                                                                                                                                                                                                                                                                 |
| WN \_ no \_ conectado  | El dispositivo no se redirige.                                                                                                                                                                                                                                                                                                           |
| WN \_ \_ archivos abiertos     | No se pudo cancelar la conexión porque los archivos todavía están abiertos.                                                                                                                                                                                                                                                                      |
| \_mala \_    | El nombre de red no es válido.                                                                                                                                                                                                                                                                                                          |



 

 

 




