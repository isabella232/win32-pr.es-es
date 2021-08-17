---
description: Representa una textura en un archivo y devuelve el resultado al host de forma asincrónica.
MS-HAID: vspixengine.IPixEngine5\_RenderTextureAsync\_UINT\_PixEngineTextureSliceIndex\_int\_float\_arr4\_float\_arr4\_BSTR\_UINT\_BSTR\_arr\_float\_arr\_UINT\_BSTR\_arr\_BOOL\_arr\_BSTR\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixEngine5::RenderTextureAsync (método)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41189637fd741d22fc566f913b25ddba1109854ed12a0336ffac899c10fd3147
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119405685"
---
# <a name="span-idvspixengineipixengine5_rendertextureasync_uint_pixenginetexturesliceindex_int_float_arr4_float_arr4_bstr_uint_bstr_arr_float_arr_uint_bstr_arr_bool_arr_bstr_ipixengine5callbacks_ptr_dword_dwordspanipixengine5rendertextureasync-method"></a><span id="vspixengine.ipixengine5_rendertextureasync_uint_pixenginetexturesliceindex_int_float_arr4_float_arr4_bstr_uint_bstr_arr_float_arr_uint_bstr_arr_bool_arr_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5::RenderTextureAsync (método)

Representa una textura en un archivo y devuelve el resultado al host de forma asincrónica.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RenderTextureAsync(
   UINT                       textureId,
   PixEngineTextureSliceIndex sliceIndex,
   int                        formatOverride,
   float [4]                  lower,
   float [4]                  upper,
   BSTR                       shaderFileName,
   UINT                       numFloatShaderVars,
   BSTR []                    count6_shaderFloatVarName,
   float []                   count6_shaderFloatVarValue,
   UINT                       numBoolShaderVars,
   BSTR []                    count9_shaderBoolVarName,
   BOOL []                    count9_shaderBoolVarValue,
   BSTR                       renderContentFileName,
   IPixEngine5Callbacks*      callbacks,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a>Parámetros

*textureId*   
Identificador de la textura que se representará.

*sliceIndex*   
Índice del segmento dentro de la textura que se representa.

*formatOverride*   
Invalidación del formato de color.

*Inferior*   

*Superior*   

*shaderFileName*   
Cadena COM que contiene el nombre de ruta de acceso del archivo de sombreador.

*numFloatShaderVars*   
Número de variables de sombreador de punto flotante

*count6 \_ shaderFloatVarName*   
Cadenas COM con los nombres de las variables de sombreador de punto flotante.

*count6 \_ shaderFloatVarValue*   
Variables del sombreador de punto flotante.

*numBoolShaderVars*   
Número de variables booleanas del sombreador.

*count9 \_ shaderBoolVarName*   
Cadenas COM que se une a los nombres de las variables booleanas del sombreador.

*count9 \_ shaderBoolVarValue*   
Variables booleanas del sombreador.

*renderContentFileName*   
Cadena COM que contiene el nombre de ruta de acceso del archivo donde se escribió la textura representado.

*Callbacks*   
Dirección de un objeto que proporciona la interfaz de devoluciones de llamada IPixEngine5.

*requestCookie*   
Cookie que identifica de forma única la solicitud y se puede usar para indicar que se cancele.

*progressIntervalMsecs*   
No se usa.

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vea también

[**IPixEngine5**](/windows/desktop/direct3dtools/ipixengine5)

 

 
