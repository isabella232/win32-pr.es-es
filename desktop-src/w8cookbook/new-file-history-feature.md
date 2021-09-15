---
title: Nueva Historial de archivos de datos
description: Nueva Historial de archivos de datos
ms.assetid: B1EE4638-5591-483B-AA09-600E242ED50B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a70aad84f4d052d6a872c7b0cfc979d0fa05cb84
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359630"
---
# <a name="new-file-history-feature"></a>Nueva Historial de archivos de datos

## <a name="platform"></a>Plataforma

**Clientes:** Windows 8 


## <a name="description"></a>Descripción

La nueva Historial de archivos reemplaza la función de copia de seguridad y restauración existente y ofrece protección para los archivos de usuario almacenados en bibliotecas de usuario. Se proporciona un conjunto de API que permite a los desarrolladores habilitar Historial de archivos mediante programación y seleccionar un destino de almacenamiento específico. La documentación de estas API está disponible en MSDN.

Puede afectar a los flujos de trabajo relacionados con la protección de datos y la documentación que dependen de la característica Copias de seguridad de Windows y restauración.

No se recomienda usar ambas características al mismo tiempo. Historial de archivos comprueba si existe una programación de copia de seguridad y está activa y, si encuentra una, no permitirá a los usuarios activarla. En este caso, los usuarios que quieran usar Historial de archivos tendrán que eliminar la Copias de seguridad de Windows programación.

## <a name="manifestation"></a>Manifestación

Los flujos de trabajo se pueden interrumpir y la documentación del método anterior para acceder a la característica Copias de seguridad de Windows y restauración deberá actualizarse para reflejar estos cambios.

## <a name="solution"></a>Solución

Revise las aplicaciones que contienen flujos de trabajo que se verán afectados negativamente por la nueva característica Historial de archivos para quitar los conflictos e incorporar el nuevo conjunto de API.

## <a name="tests"></a>Pruebas

La API permite a los desarrolladores determinar si Historial de archivos está activado.

 

 




