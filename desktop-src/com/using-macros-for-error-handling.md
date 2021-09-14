---
title: Usar macros para el control de errores
description: COM define una serie de macros que facilitan el trabajo con valores HRESULT.
ms.assetid: ad28eb80-cab9-4bec-9601-34660f6dcad4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2f31280ec2076f8ece1fcf15dd6e27629a3016e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973583"
---
# <a name="using-macros-for-error-handling"></a>Usar macros para el control de errores

COM define una serie de macros que facilitan el trabajo con **valores HRESULT.**

Las macros de control de errores se describen en la tabla siguiente.




| Macro | Descripción | 
|-------|-------------|
| <a href="/windows/desktop/api/dmerror/nf-dmerror-make_hresult"><strong>MAKE_HRESULT</strong></a><br /> | Devuelve un <strong>valor HRESULT dado</strong> el bit de gravedad, el código de instalación y el código de error que componen <strong>el HRESULT</strong>.<br /><blockquote>[!Note]<br />Llamar <a href="/windows/desktop/api/dmerror/nf-dmerror-make_hresult"><strong>MAKE_HRESULT</strong></a> para S_OK comprobación conlleva una penalización de rendimiento. No debe usar rutinariamente <strong>MAKE_HRESULT</strong> resultados correctos.</blockquote><br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-make_scode"><strong>MAKE_SCODE</strong></a><br /> | Devuelve un <strong>SCODE dado</strong> el bit de gravedad, el código de instalación y el código de error que componen <strong>SCODE.</strong><br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-hresult_code"><strong>HRESULT_CODE</strong></a><br /> | Extrae la parte del código de error del <strong>HRESULT</strong>.<br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-hresult_facility"><strong>HRESULT_FACILITY</strong></a><br /> | Extrae el código de instalación del <strong>HRESULT</strong>.<br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-hresult_severity"><strong>HRESULT_SEVERITY</strong></a><br /> | Extrae el bit de gravedad del <strong>HRESULT</strong>.<br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-scode_code"><strong>SCODE_CODE</strong></a><br /> | Extrae la parte del código de error de <strong>SCODE.</strong><br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-scode_facility"><strong>SCODE_FACILITY</strong></a><br /> | Extrae el código de instalación de <strong>SCODE.</strong><br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-scode_severity"><strong>SCODE_SEVERITY</strong></a><br /> | Extrae el campo de gravedad de <strong>SCODE.</strong><br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-succeeded"><strong>TUVO ÉXITO</strong></a><br /> | Comprueba el bit de gravedad de <strong>SCODE</strong> o <strong>HRESULT</strong>; devuelve <strong>TRUE</strong> si la gravedad es cero y <strong>FALSE</strong> si es uno.<br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-failed"><strong>FALLADO</strong></a><br /> | Comprueba el bit de gravedad de <strong>SCODE</strong> o <strong>HRESULT</strong>; devuelve <strong>TRUE</strong> si la gravedad es uno y <strong>FALSE</strong> si es cero.<br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-is_error"><strong>IS_ERROR</strong></a><br /> | Proporciona una prueba genérica de errores en cualquier valor de estado. <br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-hresult_from_win32"><strong>HRESULT_FROM_WIN32</strong></a><br /> | Mapas código <a href="/windows/desktop/Debug/system-error-codes">de error del sistema</a> a un valor <strong>HRESULT.</strong> <br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-hresult_from_nt"><strong>HRESULT_FROM_NT</strong></a><br /> | Mapas un valor de estado NT a <strong>un valor HRESULT.</strong><br /> | 




 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Control de errores en COM](error-handling-in-com.md)
</dt> </dl>

 

