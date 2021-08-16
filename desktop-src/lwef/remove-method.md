---
title: Remove (método)
description: Remove (método)
ms.assetid: b50d47b2-a425-4545-8d85-efeae460d2b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3337fb25db49f1d6c8ccd6d94f2817340db226e14718cfa7943940fbfb069b07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117882786"
---
# <a name="remove-method"></a>Remove (método)

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Quita un [**objeto Command**](/windows/desktop/lwef/the-command-object) de la colección [**Commands.**](/windows/desktop/lwef/the-commands-collection-object)

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent***. Caracteres ("**_CharacterID_*_"). Commands.Remove_ * _Name_



| Parte   | Descripción                                                       |
|--------|-------------------------------------------------------------------|
| *Nombre* | Obligatorio. Valor de cadena correspondiente al identificador del comando. |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

Cuando se quita un objeto [**Command**](/windows/desktop/lwef/the-command-object) de la colección, ya no aparece cuando se muestra el menú emergente del carácter o en la ventana Comandos cuando la aplicación cliente está activa en la entrada.

## <a name="see-also"></a>Consulte también

[**método RemoveAll**](removeall-method.md)


 

 