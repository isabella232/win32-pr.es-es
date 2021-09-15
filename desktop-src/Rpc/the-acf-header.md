---
title: El encabezado ACF
description: El encabezado ACF contiene atributos específicos de la plataforma que se aplican a la interfaz en su conjunto. Los atributos aplicados a tipos y funciones individuales en el cuerpo de ACF invalidan los atributos del encabezado ACF. No se requiere ningún atributo en el encabezado ACF.
ms.assetid: c09ec0f2-2302-450a-b74b-c9008beca325
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64e958044f043db8828f0fdda192918c632c321b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476584"
---
# <a name="the-acf-header"></a>El encabezado ACF

El encabezado ACF contiene atributos específicos de la plataforma que se aplican a la interfaz en su conjunto. Los atributos aplicados a tipos y funciones individuales en el cuerpo de ACF invalidan los atributos del encabezado ACF. No se requiere ningún atributo en el encabezado ACF.

El encabezado ACF puede incluir uno de los atributos siguientes: **\[** [**identificador automático, \_**](/windows/desktop/Midl/auto-handle)identificador **\]** **\[** [**\_ implícito**](/windows/desktop/Midl/implicit-handle) **\]** o identificador [**\_ explícito.**](/windows/desktop/Midl/explicit-handle) **\]** Si **\[ se \_ usa \]** **\[ \_ \] el** identificador automático o el identificador implícito, especifica el tipo de identificador de enlace que se usará para el enlace cuando una función remota no tenga un parámetro de identificador de enlace explícito. Cuando el ACF no está presente o no especifica un identificador de enlace automático, implícito o explícito, MIDL **\[ \_ \]** usa el identificador automático para el enlace implícito.

El **\[** [**código**](/windows/desktop/Midl/code) **\]** o el código **\[** [**nocode**](/windows/desktop/Midl/nocode) pueden aparecer en el encabezado de interfaz, pero el que elija solo puede aparecer una **\]** vez. Cuando ninguno de los atributos está presente, el compilador **\[ usa el código \]** como valor predeterminado.

Para obtener más información, vea [Atributos de ACF.](/windows/desktop/Midl/acf-attributes)

 

 