---
description: Devuelve valores que un proveedor de red puede establecer.
ms.assetid: f8e6692f-4824-40fe-a5b3-9843689ea02e
title: Valores devueltos de seguridad de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a40fd8e6e21d9e7671c1e7b9c3d008978628e28cb0fcb01c3df56359144e72e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921304"
---
# <a name="network-security-return-values"></a>Valores devueltos de seguridad de red

Los valores devueltos que un proveedor de red puede establecer incluyen los siguientes códigos de error.



| Códigos de error         | Descripción                                                                                                                                                                                                                                                                                                                             |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WN \_ SUCCESS         | La función se ha realizado correctamente.                                                                                                                                                                                                                                                                                                                 |
| WN \_ NO \_ COMPATIBLE  | La función no se admite en este proveedor de red.                                                                                                                                                                                                                                                                                 |
| ERROR DE WN \_ NET \_      | Se produjo un error de red desconocido.                                                                                                                                                                                                                                                                                                       |
| WN \_ MORE \_ DATA      | El búfer de datos pasado no es suficiente para contener todos los datos disponibles.                                                                                                                                                                                                                                                         |
| PUNTERO NO VÁLIDO DE WN \_ \_    | Se especificó un puntero que no es válido durante la llamada de función.                                                                                                                                                                                                                                                                     |
| VALOR NO VÁLIDO DE WN \_ \_      | Se especificó un valor numérico que no es válido durante la llamada de función.                                                                                                                                                                                                                                                               |
| CONTRASEÑA INCORRECTA DE WN \_ \_   | Se especificó una contraseña incorrecta.                                                                                                                                                                                                                                                                                                    |
| ACCESO \_ DENEGADO DE WN \_  | El autor de la llamada no tiene permisos suficientes para completar la operación.                                                                                                                                                                                                                                                              |
| WN \_ FUNCTION \_ BUSY  | Esta función no se puede volver a escribir y se está utilizando actualmente, o el proveedor todavía se está inicializando y aún no está listo para llamarse. El proveedor debe devolver este código de error solo si va a estar disponible. El MPR pasa este código de retorno a su autor de la llamada y es probable que haga que el autor de la llamada vuelva a intentarlo.<br/> |
| ERROR DE WINDOWS DE WN \_ \_  | Error en una función necesaria.                                                                                                                                                                                                                                                                                                             |
| USUARIO CON ERRORES DE WN \_ \_       | Se especificó un nombre de usuario que no es válido.                                                                                                                                                                                                                                                                                            |
| WN \_ FUERA \_ DE \_ MEMORIA | No hay memoria suficiente para completar la operación.                                                                                                                                                                                                                                                                                 |
| WN \_ NO \_ CONECTADO  | El dispositivo no se redirige.                                                                                                                                                                                                                                                                                                           |
| WN \_ OPEN \_ FILES     | No se pudo cancelar la conexión porque los archivos siguen abiertos.                                                                                                                                                                                                                                                                      |
| WN \_ BAD \_ NETNAME    | El nombre de red no es válido.                                                                                                                                                                                                                                                                                                          |



 

 

 




