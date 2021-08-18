---
description: El comportamiento predeterminado del control InkEdit es reconocer y convertir la entrada de lápiz en texto después de que haya expirado un breve tiempo de espera.
ms.assetid: d141bcec-e9a8-48b8-86cf-9476a2cc6f9f
title: Mostrar la entrada de lápiz como entrada de lápiz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de038df5c1b7e43f90ea02edc166039d606fe56761c96a47508714fd94ed6530
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709475"
---
# <a name="displaying-ink-as-ink"></a>Mostrar la entrada de lápiz como entrada de lápiz

El comportamiento predeterminado del control [InkEdit](inkedit-control-reference.md) es reconocer y convertir la entrada de lápiz en texto después de que haya expirado un breve tiempo de espera. Dado que el control es una superclase de [RichEdit](../controls/rich-edit-controls.md), también es posible insertar y mostrar entrada manuscrita dentro del control. Cada palabra se inserta en el control como [**un objeto InkDisp.**](inkdisp-class.md) El **objeto InkDisp** contiene la entrada de lápiz y sus alternativas de reconocimiento.

Cuando se inserta, la entrada de lápiz se escala al tamaño de fuente actual y se aplican otras propiedades ambientales, como cursiva o negrita. Si el usuario decide editar el texto de un objeto [**InkDisp,**](inkdisp-class.md) primero debe convertir la entrada de lápiz en texto.

> [!Note]  
> Todos los datos alternativos de entrada de lápiz y reconocimiento se pierden durante la conversión.

 

Esta característica solo está disponible en equipos que ejecutan Microsoft Windows XP Tablet PC Edition, Windows Vista o versiones posteriores.

 

 
