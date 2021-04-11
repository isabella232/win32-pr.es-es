---
title: Atributos de lista predefinidos (TsAttrid. h)
description: Los valores siguientes identifican los atributos de lista obtenidos con el método ITfContext GetAppProperty. Se incluyen el formato de datos y el contenido de cada tipo de propiedad.
ms.assetid: 9a9e1912-51c0-40e0-9e3a-b84ea7077dbe
keywords:
- Atributos de lista predefinidos marco de trabajo de servicios de texto
topic_type:
- apiref
api_name:
- Predefined List Attributes
api_location:
- TsAttrid.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81ade2403e124b934c6872f39c01fc7fc1ea6f6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150854"
---
# <a name="predefined-list-attributes"></a>Atributos de lista predefinidos

Los valores siguientes identifican los atributos de lista obtenidos con el método [ITfContext:: GetAppProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty) . Se incluyen el formato de datos y el contenido de cada tipo de propiedad.

## <a name="properties"></a>Propiedades



| Propiedad                          | Descripción                                                                                     |
|-----------------------------------|-------------------------------------------------------------------------------------------------|
| Lista de TSATTRID \_                    | No se utiliza.                                                                                       |
| TSATTRID \_ lista \_ LevelIndel        | Contiene el nivel de índice de la lista. 1 es el nivel más externo, 2 es el nivel siguiente, y así sucesivamente. |
| \_Tipo de lista TSATTRID \_              | No se utiliza.                                                                                       |
| \_Tipo de lista TSATTRID \_ \_ Árabe      | Contiene un valor distinto de cero si la lista es una lista de números arábigos o cero en caso contrario.               |
| \_Viñeta de \_ tipo de lista de TSATTRID \_      | Contiene un valor distinto de cero si la lista es una lista con viñetas o cero en caso contrario.                      |
| \_Tipo de lista TSATTRID \_ \_ LowerLetter | Contiene un valor distinto de cero si la lista es una lista con letras minúsculas o cero en caso contrario.            |
| \_Tipo de lista TSATTRID \_ \_ LowerRoman  | Contiene un valor distinto de cero si la lista es una lista de números romanos en minúsculas o cero en caso contrario.       |
| \_Tipo de lista TSATTRID \_ \_ UpperLetter | Contiene un valor distinto de cero si la lista es una lista con letras mayúsculas o cero en caso contrario.          |
| Tipo de lista TSATTRID de \_ \_ \_ perro  | Contiene un valor distinto de cero si la lista es una lista de números romanos en mayúsculas o cero en caso contrario.      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Redistribuible<br/>          | TSF 1,0 en Windows 2000 Professional<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>TsAttrid. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ITfContext::GetAppProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty)
</dt> </dl>

 

