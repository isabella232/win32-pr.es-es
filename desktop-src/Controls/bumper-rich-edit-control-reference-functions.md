---
title: Funciones rich edit
description: Funciones rich edit
ms.assetid: 5e913cb6-d561-447f-b33e-9160a8f46cda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df1b74069b63220a07bfb1bd5e3f5a1ad99a6c6c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482461"
---
# <a name="rich-edit-functions"></a>Funciones rich edit

## <a name="in-this-section"></a>En esta sección




| Tema | Descripción | 
|-------|-------------|
| <a href="/windows/desktop/api/Richedit/nc-richedit-autocorrectproc"><em>AutoCorrectProc</em></a><br /> | La <a href="/windows/desktop/api/Richedit/nc-richedit-autocorrectproc"><em>función AutoCorrectProc</em></a> es una función de devolución de llamada definida por la aplicación que se usa con el <a href="em-setautocorrectproc.md"><strong>EM_SETAUTOCORRECTPROC</strong></a> mensaje.<br /> | 
| <a href="/windows/desktop/api/Richedit/nc-richedit-editstreamcallback"><em>EditStreamCallback</em></a><br /> | La <a href="/windows/desktop/api/Richedit/nc-richedit-editstreamcallback"><em>función EditStreamCallback es</em></a> una función de devolución de llamada definida por la aplicación que se usa con EM_STREAMIN y <a href="em-streamin.md"><strong></strong></a> <a href="em-streamout.md"><strong>EM_STREAMOUT</strong></a> mensajes. Se usa para transferir un flujo de datos dentro o fuera de un control de edición enriquecido. El <strong>tipo EDITSTREAMCALLBACK</strong> define un puntero a esta función de devolución de llamada. <em>EditStreamCallback es</em> un marcador de posición para el nombre de función definido por la aplicación. <br /> | 
| <a href="/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex"><em>EditWordBreakProcEx</em></a><br /> | La <a href="/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex"><em>función EditWordBreakProcEx</em></a> es una función de devolución de llamada definida por la aplicación que se usa con <a href="em-setwordbreakprocex.md"><strong>EM_SETWORDBREAKPROCEX</strong></a> mensaje. Determina el índice de caracteres de la palabra break o la clase de caracteres y las marcas de salto de palabras de los caracteres del texto especificado. El <strong>tipo EDITWORDBREAKPROCEX</strong> define un puntero a esta función de devolución de llamada. <em>EditWordBreakProcEx es</em> un marcador de posición para el nombre de la función definida por la aplicación. <br /> | 
| <a href="/previous-versions/windows/desktop/legacy/hh780353(v=vs.85)"><strong>GetMathAlphanumeric</strong></a><br /> | Recupera el carácter alfanumérico matemático formato de transformación Unicode (UTF)-32 que corresponde al carácter plano multilingüe básico (BMP) y al estilo matemático especificados. <br /> | 
| <a href="/previous-versions/windows/desktop/legacy/hh780354(v=vs.85)"><strong>GetMathAlphanumericCode</strong></a><br /> | Recupera el estilo matemático y el código de carácter plano multilingüe básico (BMP) vertical que corresponde al byte final especificado de un par suplente matemático.<br /> | 
| <a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>HyphenateProc</em></a><br /> | La <a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>función HyphenateProc</em></a> es una función de devolución de llamada definida por la aplicación que se usa con <a href="em-sethyphenateinfo.md"><strong>EM_SETHYPHENATEINFO</strong></a> mensaje. Determina cómo se realiza la separación de guiones en un control De edición enriquecte de Microsoft.<br /> | 
| <a href="/previous-versions/windows/desktop/legacy/hh780443(v=vs.85)"><strong>MathBuildDown</strong></a><br /> | Convierte los objetos matemáticos, ruby y otros objetos en línea integrados del intervalo especificado a forma lineal.<br /> | 
| <a href="/previous-versions/windows/desktop/legacy/hh780445(v=vs.85)"><strong>MathBuildUp</strong></a><br /> | Convierte la matemática de formato lineal de un intervalo en un formulario integrado o modifica el formulario integrado actual. <br /> | 
| <a href="/previous-versions/windows/desktop/legacy/hh780446(v=vs.85)"><strong>MathTranslate</strong></a><br /> | Convierte los caracteres matemáticos en el intervalo especificado.<br /> | 
| <a href="reextendedregisterclass.md"><strong>REExtendedRegisterClass</strong></a><br /> | Registra dos nombres de clase, REListBox20W y RECombobox20W, que podrían usarse para crear ventanas de cuadro de lista De edición enriquecedir o cuadro combinado. <br /><blockquote>[!Note]<br />Destinado a uso interno; no se recomienda para su uso en aplicaciones. Es posible que esta función no se pueda usar en versiones futuras.</blockquote><br /> | 




 

 

