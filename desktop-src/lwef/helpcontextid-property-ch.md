---
title: Propiedad HelpContextID (objeto Characters)
description: Propiedad HelpContextID
ms.assetid: 7ef190ba-c194-4386-a8d6-d32d902a1c03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42006f74cc3668f8df9af2c2ffcd2515614ec735
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104421797"
---
# <a name="helpcontextid-property-characters-object"></a>Propiedad HelpContextID (objeto Characters)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Devuelve o establece un número de contexto asociado para el carácter. Se utiliza para proporcionar ayuda contextual para el carácter.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*Caracteres Agent. ***("**_CharacterID_*_")._ *  \[  =  *Número* de HelpContextID\]



| Parte     | Descripción                                   |
|----------|-----------------------------------------------|
| *Number* | Entero que especifica un número de contexto válido. |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para admitir la ayuda contextual para el carácter, asigne el número de contexto al carácter que se usa para el tema de ayuda asociado al compilar el archivo de ayuda. Esta propiedad solo se aplica al cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres del cliente.

Si ha creado un archivo de ayuda de Windows para la aplicación y ha establecido la propiedad [**HelpFile**](helpfile-property.md) del carácter, el agente llama automáticamente a Help cuando [**HelpModeOn**](helpmodeon-property.md) está establecido en **true** y el usuario hace clic en el carácter. Si hay un número de contexto en el [**HelpContextID**](helpcontextid-property.md), el agente llama a help y busca el tema identificado por el número de contexto actual. El número de contexto actual es el valor de **HelpContextID** para el carácter.

> [!Note]  
> La compilación de un archivo de ayuda requiere el compilador de ayuda de Microsoft Windows.

 

## <a name="see-also"></a>Consulte también

[**HelpFile (propiedad)**](helpfile-property.md)


 

 




