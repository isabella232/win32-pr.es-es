---
title: Definición de la interfaz
description: Una definición de interfaz es una especificación formal de cómo una aplicación cliente y una aplicación de servidor se comunican entre sí.
ms.assetid: 709ca498-4da3-4e6f-bb12-333a407b74c2
keywords:
- Llamada a procedimiento remoto RPC , tareas, definición de la interfaz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9f447847eeca39258b96ba129c46b3f7bcf054
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069148"
---
# <a name="defining-the-interface"></a>Definición de la interfaz

Una definición de interfaz es una especificación formal de cómo una aplicación cliente y una aplicación de servidor se comunican entre sí. La interfaz define cómo el cliente y el servidor se reconocen entre sí, los procedimientos remotos a los que puede llamar la aplicación cliente y los tipos de datos de los parámetros y valores devueltos de esos procedimientos. También especifica cómo se transmiten los datos entre el cliente y el servidor.

Esta interfaz se define en Lenguaje de definición de interfaz de Microsoft (MIDL), que consta de definiciones de lenguaje C aumentadas con palabras clave, denominadas atributos, que describen cómo se transmiten los datos a través de la red.

El archivo de definición de interfaz (IDL) contiene definiciones de tipo, atributos y prototipos de función que describen cómo se transmiten los datos en la red. El archivo de configuración de la aplicación (ACF) contiene atributos que configuran la aplicación para un entorno operativo determinado sin que ello afecte a sus características de red.

 

 




