---
title: Propiedad MoveCause
description: Propiedad MoveCause
ms.assetid: 8f78a6da-8498-4a39-a4b9-5ab7a43d97f5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa797338e64edfd67ae2347f2983df624464df923a64883e3adc5143671b15dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117883836"
---
# <a name="movecause-property"></a>Propiedad MoveCause

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Devuelve un valor entero que especifica lo que produjo el último movimiento del carácter.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agente*. **Characters("**_CharacterID_*_"). MoveCause_*



| Valor | Descripción                                                                                |
|-------|--------------------------------------------------------------------------------------------|
| 0     | El carácter no se ha movido.                                                          |
| 1     | El usuario movió el carácter.                                                              |
| 2     | La aplicación movió el carácter.                                                      |
| 3     | Otra aplicación cliente movió el carácter.                                            |
| 4     | El servidor del Agente movió el carácter para mantenerlo en pantalla después de un cambio de resolución de pantalla. |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

Puede usar esta propiedad para determinar qué hizo que el carácter se mueva, cuando más de una aplicación comparte (ha cargado) el mismo carácter. Estos valores son los mismos que los devueltos por el [**evento Move.**](move-event.md)

## <a name="see-also"></a>Consulte también

[**Evento Move**](move-event.md), [ **método MoveTo**](moveto-method.md)


 

 




