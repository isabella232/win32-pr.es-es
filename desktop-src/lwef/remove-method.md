---
title: Remove (método)
description: Remove (método)
ms.assetid: b50d47b2-a425-4545-8d85-efeae460d2b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52f7fc80954a1ffe218ba38405a551e5f000dc76
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358974"
---
# <a name="remove-method"></a>Remove (método)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Quita un objeto [**Command**](/windows/desktop/lwef/the-command-object) de la colección [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*agente ***. Caracteres ("*** CharacterID ***"). Commands. Remove*** Name*



| Parte   | Descripción                                                       |
|--------|-------------------------------------------------------------------|
| *Nombre* | Obligatorio. Valor de cadena que corresponde al identificador del comando. |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Cuando se quita un objeto de [**comando**](/windows/desktop/lwef/the-command-object) de la colección, ya no aparece cuando se muestra el menú emergente del carácter o en la ventana comandos cuando la aplicación cliente es de entrada-activa.

## <a name="see-also"></a>Consulte también

[**método RemoveAll**](removeall-method.md)


 

 