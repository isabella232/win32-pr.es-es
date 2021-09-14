---
title: Etiqueta Lst
description: Etiqueta Lst
ms.assetid: 82246675-9aa1-4603-a8f7-a5fd7b3f6be2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecf13da7bf0267941939ec22c12706ed8c75c27e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361201"
---
# <a name="lst-tag"></a>Etiqueta Lst

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Repite la última instrucción hablada para el carácter.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

\\**Lst**\\

</dd> </dl>

### <a name="remarks"></a>Observaciones

Esta etiqueta permite que un carácter repita su última instrucción hablada. Esta etiqueta debe aparecer por sí misma en el [**método Speak;**](speak-method.md) no se puede incluir ningún otro texto o parámetro. Cuando se repite el texto hablado, se repiten las demás etiquetas incluidas en el texto original, excepto los marcadores. Cualquier. WAV y . Los archivos LWV incluidos en el texto también se repiten.

 

 




