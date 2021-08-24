---
description: Analiza texto para identificar palabras y proporciona los resultados al objeto WordSink.
ms.assetid: 42bfc961-c095-4380-9b55-b58a0d9f2c00
title: IWordInfo::BreakText (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordInfo.BreakText
api_type:
- COM
api_location:
- Msir3jp.dll
ms.openlocfilehash: 4cb4e4b27b52a4fb22a65f382a20c51a43ca5c77feb14828a7ea252e75c3b0f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749745"
---
# <a name="iwordinfobreaktext-method"></a>IWordInfo::BreakText (método)

\[Este método está obsoleto y no se admite en Windows Vista.\]

Analiza texto para identificar palabras y proporciona los resultados al [objeto WordSink.](/previous-versions//ms691570(v=vs.85))

## <a name="syntax"></a>Sintaxis


```C++
HRESULT BreakText(
  [in] TEXT_SOURCE *pTextSource,
  [in] IWordSink   *pWordSink,
  [in] DWORD       fBreakMode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pTextSource* \[ En\]
</dt> <dd>

Puntero a una [estructura TEXT \_ SOURCE](/previous-versions//ms690919(v=vs.85)) que contiene el texto Unicode.

</dd> <dt>

*pWordSink* \[ En\]
</dt> <dd>

Puntero al objeto [WordSink](/previous-versions//ms691570(v=vs.85)) que recibe y controla las palabras generadas por este método. Si este parámetro es **NULL,** el método no divide la cadena en palabras.

</dd> <dt>

*fBreakMode* \[ En\]
</dt> <dd>

Modo de interrupción. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                                                                                                                   | Significado                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="IWORDINFO_BREAKTEXTMODE_DICTFORM"></span><span id="iwordinfo_breaktextmode_dictform"></span><dl> <dt>**IWORDINFO \_ BREAKTEXTMODE \_ DICTFORM**</dt> <dt>0x00000002</dt> </dl> | Word break the text string and pass the dictionary form of the words to the **WordSink** object.<br/> |
| <span id="IWORDINFO_BREAKTEXTMODE_SMARTSEL"></span><span id="iwordinfo_breaktextmode_smartsel"></span><dl> <dt>**IWORDINFO \_ BREAKTEXTMODE \_ SMARTSEL**</dt> <dt>0x00000001</dt> </dl> | Word separa la cadena de texto y pasa las palabras al **objeto WordSink.**<br/>                        |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve uno de los valores siguientes.



| Código devuelto                                                                            | Descripción                                                                                             |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | La operación se realizó correctamente. No hay más texto disponible para rellenar el *búfer pTextSource.*<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | El *parámetro pTextSource* es **NULL.**<br/>                                                     |



 

## <a name="remarks"></a>Comentarios

Use el **miembro pfnFillTextBuffer de** la **estructura TEXT \_ SOURCE** para reponer el texto de origen. Este método debe controlar todos los valores devueltos de la función de devolución de llamada **pfnFillTextBuffer.** Si se produce un error, finalice el procesamiento del texto en el búfer antes de controlar el error.

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

[**IWordInfo**](iwordinfo.md)
</dt> <dt>

[ORIGEN DE \_ TEXTO](/previous-versions//ms690919(v=vs.85))
</dt> <dt>

[**WordInfo**](wordinfo-coclass.md)
</dt> <dt>

[WordSink](/previous-versions//ms691570(v=vs.85))
</dt> </dl>

 

 
