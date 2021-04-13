---
description: La interfaz IWordInfo es un componente de recurso de idioma específico para japonés. El objeto analiza el texto e identifica las palabras individuales, devolviendo las palabras de la cadena o devuelve las formas de diccionario (raíz) de las palabras en el texto de la cadena.
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
ms.openlocfilehash: 9d685f2aa1b4ba4d31f221812c12729e4e689360
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538385"
---
# <a name="iwordinfo-interface"></a>Interfaz IWordInfo

\[Esta interfaz está obsoleta y no se admite en Windows Vista.\]

La interfaz **IWordInfo** es un componente de recurso de idioma específico para japonés. El objeto analiza el texto e identifica las palabras individuales, devolviendo las palabras de la cadena o devuelve las formas de diccionario (raíz) de las palabras en el texto de la cadena.

## <a name="members"></a>Miembros

La interfaz **IWordInfo** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IWordInfo** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IWordInfo** tiene estos métodos.



| Método        | Descripción                                                                                                                                 |
|:--------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| **BreakText** | Analiza el texto para identificar palabras y proporciona los resultados al objeto [WordSink](/previous-versions//ms691570(v=vs.85)) .<br/> |



 

## <a name="remarks"></a>Observaciones

Esta interfaz se utiliza para recuperar los saltos de palabra japoneses o los formatos de diccionario para el texto que se va a analizar. La forma de Diccionario de una palabra es la forma no conjugada de la palabra.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                   |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                  |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                         |
| Archivo DLL<br/>                      | <dl> <dt>Msir3jp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**WordInfo**](wordinfo-coclass.md)
</dt> <dt>

[WordSink](/previous-versions//ms691570(v=vs.85))
</dt> </dl>

 

 
