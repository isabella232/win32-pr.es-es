---
title: Nueva característica de historial de archivos
description: Nueva característica de historial de archivos
ms.assetid: B1EE4638-5591-483B-AA09-600E242ED50B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a70aad84f4d052d6a872c7b0cfc979d0fa05cb84
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "104149688"
---
# <a name="new-file-history-feature"></a>Nueva característica de historial de archivos

## <a name="platform"></a>Plataforma

**Clientes** : Windows 8 


## <a name="description"></a>Descripción

La nueva característica de historial de archivos reemplaza a la función de copia de seguridad y restauración existente y ofrece protección para los archivos de usuario almacenados en las bibliotecas de usuario. Se proporciona un conjunto de API que permite a los desarrolladores habilitar mediante programación el historial de archivos y seleccionar un destino de almacenamiento específico. La documentación de estas API está disponible en MSDN.

Puede afectar a los flujos de trabajo relacionados con la protección de datos y la documentación que dependen de la característica copia de seguridad y restauración de Windows.

No se recomienda usar ambas características al mismo tiempo. El historial de archivos comprueba si existe una programación de copia de seguridad y está activa y, si encuentra alguna, no permitirá que los usuarios la activen. En este caso, los usuarios que deseen usar el historial de archivos tendrán que eliminar la programación de copias de seguridad de Windows.

## <a name="manifestation"></a>Manifestación

Los flujos de trabajo se pueden interrumpir y la documentación del método anterior para tener acceso a la característica copia de seguridad y restauración de Windows deberá actualizarse para reflejar estos cambios.

## <a name="solution"></a>Solución

Revise las aplicaciones que contienen flujos de trabajo que se ven perjudicados por la nueva característica de historial de archivos para quitar los conflictos e incorporar el nuevo conjunto de API.

## <a name="tests"></a>Pruebas

La API permite a los desarrolladores determinar si el historial de archivos está activado.

 

 




