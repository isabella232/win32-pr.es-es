---
title: IAgentCharacterEx GetSRModeID
description: IAgentCharacterEx GetSRModeID
ms.assetid: 28049680-8245-49f3-9ecd-13c7605f10ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0bba237fb1bc1b5d769f7e8ecf983b58718c18e
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "103788998"
---
# <a name="iagentcharacterexgetsrmodeid"></a>IAgentCharacterEx::GetSRModeID

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetSRModeID(
   BSTR * pbszModeID  // address of speech recognition engine ID
);
```

Recupera el identificador de modo del conjunto de motores de reconocimiento de voz para el carácter.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="pbszModeID"></span><span id="pbszmodeid"></span><span id="PBSZMODEID"></span>*pbszModeID*
</dt> <dd>

Dirección de un BSTR que recibe la configuración de ID. de modo del motor de reconocimiento de voz para el carácter.

</dd> </dl>

Esta configuración devuelve el conjunto de motores para la entrada de voz de un carácter. El identificador de modo de un motor de reconocimiento de voz es una representación de cadena del GUID (con formato de llaves y guiones) por parte del proveedor de voz que identifica el motor de forma exclusiva. Para obtener más información, consulte la [documentación del SDK de Microsoft Speech](https://msdn.microsoft.com/library/ee705648.aspx).

Si no establece un identificador de modo de motor de reconocimiento de voz para el carácter, el servidor devuelve un motor que coincide con la configuración de idioma del carácter (mediante interfaces de Microsoft Speech API). Si no hay ningún motor de reconocimiento de voz coincidente disponible para el carácter, el servidor devuelve una cadena nula (vacía).

Cuando se habilita la entrada de voz (en la ventana Opciones de caracteres avanzadas), al consultar o establecer esta propiedad se cargará el motor asociado (si aún no está cargado) y se iniciarán los servicios de voz. Es decir, la clave de escucha está disponible y la sugerencia de escucha es visible. (La clave de escucha y la sugerencia de escucha solo están habilitadas si también están habilitadas en opciones de caracteres avanzadas). Sin embargo, si consulta la propiedad cuando la voz está deshabilitada, el servidor no inicia Speech Services y devuelve una cadena nula (cadena vacía).

Esta función solo devuelve el valor del uso de la aplicación cliente del carácter; la configuración no refleja otros clientes del carácter u otros caracteres de la aplicación cliente.

Esta función no genera un error si [**IAgentSpeechInputProperties:: GetEnabled**](iagentspeechinputproperties--getenabled.md) devuelve **false**.

Los requisitos del motor de voz de Microsoft Agent se basan en Microsoft Speech API. Los motores que admiten los requisitos de SAPI de Microsoft Agent se pueden instalar y usar con el agente.

## <a name="see-also"></a>Consulte también

[**IAgentCharacterEx::SetSRModeID**](iagentcharacterex--setsrmodeid.md)


 

 




