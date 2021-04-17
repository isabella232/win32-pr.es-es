---
description: El comportamiento predeterminado del control InkEdit es reconocer y convertir la entrada manuscrita en texto después de que haya expirado un breve tiempo de espera.
ms.assetid: d141bcec-e9a8-48b8-86cf-9476a2cc6f9f
title: Mostrar la entrada de lápiz como entrada de lápiz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aca1d6a1a4700d996d65a9cfd7d62e6b27e1c71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697566"
---
# <a name="displaying-ink-as-ink"></a>Mostrar la entrada de lápiz como entrada de lápiz

El comportamiento predeterminado del control [InkEdit](inkedit-control-reference.md) es reconocer y convertir la entrada manuscrita en texto después de que haya expirado un breve tiempo de espera. Dado que el control es una superclase de [RichEdit](../controls/rich-edit-controls.md), también es posible incrustar y mostrar la entrada de lápiz en el control. Cada palabra se inserta en el control como un objeto [**InkDisp**](inkdisp-class.md) . El objeto **InkDisp** contiene la tinta y sus alternativas de reconocimiento.

Cuando se inserta, la tinta se escala hasta el tamaño de fuente actual y se aplican otras propiedades de ambiente, como cursiva o negrita. Si el usuario decide editar el texto de un objeto [**InkDisp**](inkdisp-class.md) , primero debe convertir la tinta en texto.

> [!Note]  
> Todos los datos alternativos de reconocimiento y de entrada de lápiz se pierden durante la conversión.

 

Esta característica solo está disponible en equipos que ejecutan Microsoft Windows XP Tablet PC Edition, Windows Vista o posterior.

 

 
