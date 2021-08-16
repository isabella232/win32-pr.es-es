---
description: El operador de asignación CHString (=) reinicializa un objeto CHString existente con nuevos datos.
ms.assetid: 6864aacf-ac18-4b5a-be3e-3a0d8bb31e74
ms.tgt_platform: multiple
title: CHString::operator= (ChString.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dde67bbf0f1a7326074bc7638cdd6b256ad763e115ad12e2c193e6bcdc66605e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131787"
---
# <a name="chstringoperator"></a>CHString::operator=

\[La [**clase CHString**](chstring.md) forma parte del marco de proveedores WMI que ahora se considera en estado final y no habrá más desarrollos, mejoras o actualizaciones disponibles para problemas no relacionados con la seguridad que afecten a estas bibliotecas. Las [API de MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) deben usarse para todo el desarrollo nuevo.\]

El [**operador de asignación CHString**](chstring.md) (=) reinicializa un objeto CHString existente con nuevos datos.

``` syntax
const CHString& operator =(
  const CHString& stringSrc )
throw( CHeap_Exception );

const CHString& operator =(
  WCHAR ch )
throw( CHeap_Exception );

const CHString& operator =(
  const unsigned char* psz )
throw( CHeap_Exception );

const CHString& operator =(
  LPCWSTR lpsz )
throw( CHeap_Exception );

const CHString& operator =(
  LPCSTR lpsz )
throw( CHeap_Exception );

const CHString& operator =(
  CHString *p )
throw( CHeap_Exception );

const CHString& operator =(
  char ch )
throw( CHeap_Exception );
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="stringSrc__p"></span><span id="stringsrc__p"></span><span id="STRINGSRC__P"></span>*stringSrc*, *p*
</dt> <dd>

Asigna una [**cadena CHString**](chstring.md) a este objeto .

</dd> <dt>

<span id="ch"></span><span id="CH"></span>*Ch*
</dt> <dd>

Asigna un carácter a este objeto.

</dd> <dt>

<span id="lpsz__psz"></span><span id="LPSZ__PSZ"></span>*lpsz*, *psz*
</dt> <dd>

Asigna una **cadena terminada** en NULL a este objeto.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Si la cadena de destino (es decir, el lado izquierdo) ya es lo suficientemente grande como para almacenar los nuevos datos, no se realiza ninguna nueva asignación de memoria. Sin embargo, pueden producirse excepciones de memoria cada vez que se usa el operador de asignación porque a menudo se asigna nuevo almacenamiento para contener el [**objeto CHString**](chstring.md) resultante.

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se muestra el uso de **CHString::operator =**:


```C++
CHString s1, s2;        // Empty CHString objects

s1 = L"cat";            // s1 = "cat"
s2 = s1;                // s1 and s2 each = "cat"
s1 = L"the " + s1;      // Or expressions
s1 = 'x';               // Or just individual characters
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                                                                                      |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                                                                                |
| Header<br/>                   | <dl> <dt>ChString.h (incluir FwCommon.h)</dt> </dl>                                                    |
| Biblioteca<br/>                  | <dl> <dt>FrameDyn.lib</dt> </dl>                                                                       |
| Archivo DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CHString**](chstring.md)
</dt> </dl>

 

