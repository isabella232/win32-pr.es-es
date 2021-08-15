---
title: Evento Move
description: Evento Move
ms.assetid: 973e9e68-edbb-4741-b50e-57db96712df8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9938f79a0c23340c5ed34be52019afe5f9f3fa6caefb6920941cb17dc13c0fc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118476353"
---
# <a name="move-event"></a>Evento Move

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Se produce cuando se mueve un carácter.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

**Sub** *agent* \_ **Move (ByVal** *CharacterID*, **ByVal** *X*, **ByVal** *Y*, **ByVal** *Cause...))**



| Parte          | Descripción                                                                                                                                                                                                                                                                                                                                   |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Devuelve el identificador del carácter que se movió.                                                                                                                                                                                                                                                                                                   |
| *X*           | Devuelve la coordenada X (en píxeles) del borde superior de la nueva ubicación del marco de caracteres como un entero.                                                                                                                                                                                                                                         |
| *S*           | Devuelve la coordenada Y (en píxeles) del borde izquierdo de la nueva ubicación del marco de caracteres como un entero.                                                                                                                                                                                                                                        |
| *Causa*       | Devuelve un valor que indica lo que hizo que el carácter se desplazara. 1 El usuario arrastró el carácter.<br/> 2 La aplicación cliente movió el carácter.<br/> 3 Otra aplicación cliente movió el carácter.<br/> 4 El servidor del Agente movió el carácter para mantenerlo en pantalla después de un cambio en la resolución de pantalla.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Comentarios

Este evento tiene lugar cuando el usuario o una aplicación cambian la posición del carácter. Las coordenadas son relevantes para la esquina superior izquierda de la pantalla. Este evento solo se envía a los clientes del carácter (aplicaciones que han cargado el carácter).

**Vea también**

[**Propiedad MoveCause ,**](movecause-property.md) [ **evento Size**](size-event.md)

 

 





