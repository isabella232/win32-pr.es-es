---
title: El encabezado ACF
description: El encabezado ACF contiene atributos específicos de la plataforma que se aplican a la interfaz en conjunto. Los atributos que se aplican a tipos y funciones individuales en el cuerpo ACF invalidan los atributos del encabezado ACF. No se requiere ningún atributo en el encabezado ACF.
ms.assetid: c09ec0f2-2302-450a-b74b-c9008beca325
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64e958044f043db8828f0fdda192918c632c321b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078031"
---
# <a name="the-acf-header"></a>El encabezado ACF

El encabezado ACF contiene atributos específicos de la plataforma que se aplican a la interfaz en conjunto. Los atributos que se aplican a tipos y funciones individuales en el cuerpo ACF invalidan los atributos del encabezado ACF. No se requiere ningún atributo en el encabezado ACF.

El encabezado ACF puede incluir uno de los siguientes atributos: **\[** [**\_ identificador automático**](/windows/desktop/Midl/auto-handle) **\]** , **\[** [**\_ identificador implícito**](/windows/desktop/Midl/implicit-handle) **\]** o [**\_ identificador explícito**](/windows/desktop/Midl/explicit-handle) **\]** . Si se usa el **\[ \_ identificador \] automático** o el **\[ \_ identificador \] implícito** , especifica el tipo de identificador de enlace que se utilizará para el enlace cuando una función remota no tenga un parámetro de identificador de enlace explícito. Cuando el ACF no está presente o no especifica un identificador de enlace automático, implícito o explícito, MIDL usa el **\[ \_ identificador \] automático** para el enlace implícito.

**\[** [](/windows/desktop/Midl/code) **\]** Puede aparecer código o **\[** [**nocode**](/windows/desktop/Midl/nocode) **\]** en el encabezado de la interfaz, pero el que elija solo puede aparecer una vez. Cuando no hay ningún atributo, el compilador utiliza el **\[ código \]** como valor predeterminado.

Para obtener más información, consulte [atributos ACF](/windows/desktop/Midl/acf-attributes).

 

 