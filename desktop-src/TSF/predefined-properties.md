---
title: Propiedades predefinidas (msctf. h)
description: Los siguientes valores identifican las propiedades definidas por TSF. Se incluyen el formato de datos y el contenido de cada tipo de propiedad.
ms.assetid: d88f2eba-4c98-4b32-96e1-cd019fe0f7ad
keywords:
- Propiedades predefinidas marco de trabajo de servicios de texto
topic_type:
- apiref
api_name:
- Predefined Properties
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 807d1be5d1cc025971ad294fac825b89a4a0a519
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686137"
---
# <a name="predefined-properties"></a>Propiedades predefinidas

Los siguientes valores identifican las propiedades definidas por TSF. Se incluyen el formato de datos y el contenido de cada tipo de propiedad.

## <a name="properties"></a>Propiedades



| Propiedad                        | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_atributo prop de GUID \_**       | Contiene un valor [**TfGuidAtom**](tfguidatom.md) que representa el **GUID** del atributo display. [**ITfCategoryMgr:: GetGUID**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid) se utiliza para convertir este valor en un **GUID**. Para obtener más información, vea [using display Attributes](using-display-attributes.md).                                                                                                                                                                                                                                                                                                                                                                             |
| **PROP de GUID \_ \_ TEXTOWNER**       | Contiene un valor [**TfGuidAtom**](tfguidatom.md) que representa el identificador de clase ( **CLSID** ) del servicio de texto que posee el texto. [**ITfCategoryMgr:: GetGUID**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid) se utiliza para convertir este valor en un **CLSID**.                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **\_LANGID de prop de GUID \_**          | Contiene un valor **DWORD** que contiene el identificador de idioma ( **LANGID** ) del texto de la palabra baja.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **\_lectura de propiedades de GUID \_**         | Contiene el texto de lectura fonético del texto que se incluye en la propiedad. Puede ser diferente del texto real. Las aplicaciones de la tienda Windows no admiten esta propiedad.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **\_composición de prop de GUID \_**       | Contiene un valor booleano que es distinto de cero si el texto forma parte de una composición o cero de lo contrario. Si esta propiedad está vacía en VT \_ , se puede suponer que el texto no forma parte de una composición.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **PROP de GUID \_ \_ MODEBIAS**        | Contiene un valor [**TfGuidAtom**](tfguidatom.md) que representa el tipo de sesgo de modo admitido. [**ITfCategoryMgr:: GetGUID**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid) se utiliza para convertir este valor en un **GUID**. Puede ser uno de los [**valores de diferencia de modo**](mode-bias-values.md).                                                                                                                                                                                                                                                                                                                                                                                                  |
| **GUID \_ prop \_ Love My lifeATTICE**       | Contiene un puntero a un objeto [**ITfLMLattice**](/windows/desktop/api/Ctffunc/nn-ctffunc-itflmlattice) .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **\_alternativas de \_ TKB de prop de GUID \_** | **A partir de Windows 8:** Contiene un valor **DWORD** establecido por el teclado táctil. Esta propiedad se puede usar en las aplicaciones y los controles de edición compatibles con TSF para identificar la naturaleza del texto en el intervalo de texto que abarca la propiedad, por ejemplo, si el texto del intervalo es el resultado de la inserción de una sugerencia de texto o de corrección. <br/> La naturaleza del texto en el intervalo de texto que abarca la propiedad también se extiende al tipo de alternativas que devolvería la interfaz [**ITfFnReconversion**](/windows/desktop/api/Ctffunc/nn-ctffunc-itffnreconversion) para ese intervalo de texto en el documento.<br/> Vea los siguientes comentarios para obtener los valores posibles de esta propiedad.<br/> |



 

## <a name="remarks"></a>Observaciones

La propiedad de **\_ alternativas de prop \_ TKB \_ de GUID** puede ser uno de los valores siguientes.



| Nombre                                     | Value      | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TKB \_ alternativo \_ estándar                | 0x00000001 | Indica que el teclado táctil ha generado una lista de posibles palabras alternativas para el texto en el intervalo que abarca la propiedad, y que ni el intervalo de texto ni las alternativas son una corrección automática o una sugerencia de texto.                                                                                                                                                                                                              |
| TKB \_ alternativas \_ para la \_ corrección     | 0x00000002 | Indica que el teclado táctil ha generado una palabra alternativa que debe reemplazar automáticamente el texto en el intervalo de texto que abarca la propiedad.<br/> El teclado táctil no aplicará la corrección automática sin que el control o la aplicación de edición le indique que lo haga. La interfaz de reconversión ([**ITfFnReconversion**](/windows/desktop/api/Ctffunc/nn-ctffunc-itffnreconversion)) debe usarse para aplicar la corrección al texto del documento.<br/> |
| TKB \_ alternativas \_ para la \_ predicción         | 0x00000003 | Indica que el intervalo de texto que abarca la propiedad es una sugerencia de texto generada por el teclado táctil y que el usuario insertó en el documento.<br/> Las predicciones alternativas adicionales también se pueden almacenar como una propiedad en el documento.<br/>                                                                                                                                                                     |
| TKB \_ alternativas \_ aplicadas a la Autocorrección \_ | 0x00000004 | Indica que el intervalo de texto que abarca la propiedad es una corrección automática proporcionada por el teclado táctil y que se aplica a través de la interfaz [**ITfFnReconversion**](/windows/desktop/api/Ctffunc/nn-ctffunc-itffnreconversion) .<br/> Este valor lo pueden usar los controles de edición o las aplicaciones, con \_ alternativas \_ de TKB para \_ la corrección continua, a fin de evitar la aplicación repetida de una corrección.<br/>                                                                               |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Redistribuible<br/>          | TSF 1,0 en Windows 2000 Professional<br/>                                      |
| Encabezado<br/>                   | <dl> <dt>Msctf. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msctf. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TfGuidAtom**](tfguidatom.md)
</dt> <dt>

[**ITfCategoryMgr:: GetGUID**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid)
</dt> <dt>

[Usar atributos para mostrar](using-display-attributes.md)
</dt> <dt>

[**Valores de sesgo de modo**](mode-bias-values.md)
</dt> <dt>

[**ITfLMLattice**](/windows/desktop/api/Ctffunc/nn-ctffunc-itflmlattice)
</dt> </dl>

 

 





