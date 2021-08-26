---
title: Evento size
description: Evento size
ms.assetid: 06089f84-8e75-475f-a492-536c83fa6730
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 146763c649ab22c59a8367e3135ee0ea277c8ae4c8e4bc58588cd70c0b5ec1c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961025"
---
# <a name="size-event"></a>Evento size

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Se produce cuando cambia el tamaño de un carácter.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

**Sub** *agent* \_ **Size (ByVal** *CharacterID*, **ByVal** *Width*, **ByVal** *Height*)



| Parte          | Descripción                                                         |
|---------------|---------------------------------------------------------------------|
| *CharacterID* | Devuelve el identificador del carácter que se movió.                         |
| *Width*       | Devuelve el nuevo ancho del marco de caracteres (en píxeles) como un entero.  |
| *Height*      | Devuelve el nuevo alto del marco de caracteres (en píxeles) como un entero. |



 

</dd> </dl>

### <a name="remarks"></a>Comentarios

Este evento tiene lugar cuando una aplicación cambia el tamaño de un carácter. Este evento solo se envía a los clientes del carácter (aplicaciones que han cargado el carácter).

### <a name="see-also"></a>Consulte también

[**Evento Move**](move-event.md)


 

 




