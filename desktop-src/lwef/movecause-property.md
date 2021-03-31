---
title: Propiedad MoveCause
description: Propiedad MoveCause
ms.assetid: 8f78a6da-8498-4a39-a4b9-5ab7a43d97f5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc7f91d068befa2b919c04818c46dbc1a48faa0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903507"
---
# <a name="movecause-property"></a>Propiedad MoveCause

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Devuelve un valor entero que especifica la causa del último movimiento del carácter.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*agente*. **Caracteres ("***CharacterID***"). MoveCause**



| Value | Descripción                                                                                |
|-------|--------------------------------------------------------------------------------------------|
| 0     | No se ha despasado el carácter.                                                          |
| 1     | El usuario ha despasado el carácter.                                                              |
| 2     | La aplicación ha cambiado el carácter.                                                      |
| 3     | Otra aplicación cliente ha cambiado el carácter.                                            |
| 4     | El servidor del agente ha quitado el carácter para mantenerlo en la pantalla después de un cambio en la resolución de pantalla. |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Puede usar esta propiedad para determinar qué causó el movimiento del carácter, cuando más de una aplicación comparte (ha cargado) el mismo carácter. Estos valores son los mismos que los devueltos por el evento de [**movimiento**](move-event.md) .

## <a name="see-also"></a>Consulte también

[**Evento Move**](move-event.md), [ **método moveTo**](moveto-method.md)


 

 




