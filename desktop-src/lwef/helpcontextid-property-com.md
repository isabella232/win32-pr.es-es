---
title: Propiedad HelpContextID (objeto Command)
description: Propiedad HelpContextID
ms.assetid: 9e30e3f7-1d12-4aa1-af0d-5a3b30f57e83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8ef0fcfb24aee7aed75f8eb794e81291207ea24
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104149830"
---
# <a name="helpcontextid-property-command-object"></a>Propiedad HelpContextID (objeto Command)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Devuelve o establece un número de contexto asociado para el objeto de [**comando**](/windows/desktop/lwef/the-command-object) . Se utiliza para proporcionar ayuda contextual para el objeto de **comando** .

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*Caracteres Agent. ***("**_CharacterID_*_"). Comandos ("")._ *  \[  =  *Número* de HelpContextID\]



| Parte     | Descripción                                   |
|----------|-----------------------------------------------|
| *Number* | Entero que especifica un número de contexto válido. |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si ha creado un archivo de ayuda de Windows para la aplicación y establece la propiedad [**HelpFile**](helpfile-property.md) del carácter en el archivo, el agente llama automáticamente a Help cuando [**HelpModeOn**](helpmodeon-property.md) está establecido en **true** y el usuario selecciona el comando. Si establece un número de contexto en el [**HelpContextID**](helpcontextid-property.md), el agente llama a help y busca el tema identificado por el número de contexto actual. El número de contexto actual es el valor de **HelpContextID** para el comando.

Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

> [!Note]  
> La compilación de un archivo de ayuda requiere el compilador de ayuda de Microsoft Windows.

 

## <a name="see-also"></a>Consulte también

[**HelpFile (propiedad)**](helpfile-property.md)


 

 
