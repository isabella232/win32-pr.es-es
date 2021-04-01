---
title: FontName (propiedad, objeto Commands)
description: FontName (propiedad)
ms.assetid: 7de3653e-9b4d-4a31-82d5-243f10e2743b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4b04fa386958a75b55f9cfc50a9149de454d48f
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104149819"
---
# <a name="fontname-property-commands-object"></a>FontName (propiedad, objeto Commands)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Devuelve o establece la fuente utilizada en el menú emergente del carácter.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*Caracteres Agent. ***("**_CharacterID_*_"). Fuente Commands. FontName_ *  \[  =  \]



| Parte   | Descripción                                      |
|--------|--------------------------------------------------|
| *Fuente* | Valor de cadena que corresponde al nombre de la fuente. |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

La propiedad **FontName** define la fuente utilizada para mostrar texto en el menú emergente del carácter. El valor predeterminado de la configuración de fuente se basa en la configuración de fuente de menú para la configuración de **LanguageID** del carácter, o bien, si no se establece, la configuración de identificador de idioma predeterminado del usuario.

Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

 

 




