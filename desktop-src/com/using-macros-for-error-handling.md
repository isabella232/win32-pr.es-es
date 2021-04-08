---
title: Usar macros para el control de errores
description: COM define una serie de macros que facilitan el trabajo con valores HRESULT.
ms.assetid: ad28eb80-cab9-4bec-9601-34660f6dcad4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6605ecc05f2d24d3671d28becd770b15d56e1413
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793966"
---
# <a name="using-macros-for-error-handling"></a>Usar macros para el control de errores

COM define una serie de macros que facilitan el trabajo con valores **HRESULT** .

Las macros de control de errores se describen en la tabla siguiente.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Macro</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/dmerror/nf-dmerror-make_hresult"><strong>MAKE_HRESULT</strong></a><br/></td>
<td>Devuelve un <strong>valor HRESULT</strong> dado el bit de gravedad, el código de la instalación y el código de error que componen el <strong>HRESULT</strong>.<br/>
<blockquote>
[!Note]<br />
La llamada a <a href="/windows/desktop/api/dmerror/nf-dmerror-make_hresult"><strong>MAKE_HRESULT</strong></a> para la comprobación de S_OK conlleva una reducción del rendimiento. No debe utilizar habitualmente <strong>MAKE_HRESULT</strong> para obtener resultados correctos.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-make_scode"><strong>MAKE_SCODE</strong></a><br/></td>
<td>Devuelve un <strong>SCODE</strong> dado el bit de gravedad, el código de la instalación y el código de error que componen el <strong>SCODE</strong>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_code"><strong>HRESULT_CODE</strong></a><br/></td>
<td>Extrae la parte del código de error de <strong>HRESULT</strong>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_facility"><strong>HRESULT_FACILITY</strong></a><br/></td>
<td>Extrae el código de instalación de <strong>HRESULT</strong>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_severity"><strong>HRESULT_SEVERITY</strong></a><br/></td>
<td>Extrae el bit de gravedad del <strong>HRESULT</strong>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-scode_code"><strong>SCODE_CODE</strong></a><br/></td>
<td>Extrae la parte del código de error del <strong>SCODE</strong>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-scode_facility"><strong>SCODE_FACILITY</strong></a><br/></td>
<td>Extrae el código de instalación del <strong>SCODE</strong>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-scode_severity"><strong>SCODE_SEVERITY</strong></a><br/></td>
<td>Extrae el campo de gravedad del <strong>SCODE</strong>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-succeeded"><strong>COMPLETA</strong></a><br/></td>
<td>Comprueba el bit de gravedad del <strong>SCODE</strong> o <strong>HRESULT</strong>; Devuelve <strong>true</strong> si la gravedad es cero y <strong>false</strong> si es uno.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-failed"><strong>ERRÓNEO</strong></a><br/></td>
<td>Comprueba el bit de gravedad del <strong>SCODE</strong> o <strong>HRESULT</strong>; Devuelve <strong>true</strong> si la gravedad es una y <strong>false</strong> si es cero.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-is_error"><strong>IS_ERROR</strong></a><br/></td>
<td>Proporciona una prueba genérica de errores en cualquier valor de estado. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_from_win32"><strong>HRESULT_FROM_WIN32</strong></a><br/></td>
<td>Asigna un <a href="/windows/desktop/Debug/system-error-codes">código de error del sistema</a> a un valor <strong>HRESULT</strong> . <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_from_nt"><strong>HRESULT_FROM_NT</strong></a><br/></td>
<td>Asigna un valor de estado de NT a un valor <strong>HRESULT</strong> .<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Control de errores en COM](error-handling-in-com.md)
</dt> </dl>

 

