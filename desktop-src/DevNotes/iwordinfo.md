---
description: La interfaz IWordInfo es un componente de recursos de lenguaje específico del japonés. El objeto analiza el texto e identifica palabras individuales, devolviendo las palabras de la cadena o devuelve las formas de diccionario (raíz) de las palabras en el texto de la cadena.
ms.assetid: 760d9c78-d564-40a2-b2e4-d538c32361ed
title: Interfaz IWordInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordInfo
- IWordInfo.BreakText
api_type:
- COM
api_location:
- Msir3jp.dll
ms.openlocfilehash: a82ff0c5d817dbec6d64d1d38d40245983877563416b30760926bb7522cd14c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001475"
---
# <a name="iwordinfo-interface"></a>Interfaz IWordInfo

\[Esta interfaz está obsoleta y no se admite en Windows Vista.\]

La **interfaz IWordInfo** es un componente de recursos de lenguaje específico del japonés. El objeto analiza el texto e identifica palabras individuales, devolviendo las palabras de la cadena o devuelve las formas de diccionario (raíz) de las palabras en el texto de la cadena.

## <a name="members"></a>Miembros

La **interfaz IWordInfo** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IWordInfo también** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IWordInfo** tiene estos métodos.



| Método        | Descripción                                                                                                                                 |
|:--------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| **BreakText** | Analiza texto para identificar palabras y proporciona los resultados al [objeto WordSink.](/previous-versions//ms691570(v=vs.85))<br/> |



 

## <a name="remarks"></a>Comentarios

Esta interfaz se usa para recuperar saltos de palabras en japonés o formularios de diccionario para el texto que se va a analizar. El formato de diccionario de una palabra es la forma sin cambios de la palabra.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                   |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                  |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                         |
| Archivo DLL<br/>                      | <dl> <dt>Msir3jp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**WordInfo**](wordinfo-coclass.md)
</dt> <dt>

[WordSink](/previous-versions//ms691570(v=vs.85))
</dt> </dl>

 

 
