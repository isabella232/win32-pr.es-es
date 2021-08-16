---
title: método Unload
description: método Unload
ms.assetid: 2ffaeea6-ff24-48b2-bc99-eba429434a30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f74f274f758e34416cc73d82963fa21fbd93b14e7b6492c693f24b763081b49f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118474503"
---
# <a name="unload-method"></a>método Unload

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Descarga los datos de caracteres para el carácter especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent***. Characters.Unload "**_CharacterID_*_"_*

</dd> </dl>

## <a name="remarks"></a>Comentarios

Use este método cuando ya no necesite un carácter para liberar la memoria usada para almacenar información sobre el carácter. Si vuelve a tener acceso al carácter, use el [**método Load.**](load-method.md)

Este método no devuelve un [**objeto Request.**](/windows/desktop/lwef/the-request-object)

 

 