---
description: Las aplicaciones pueden usar Unicode para representar cadenas en varios formularios.
ms.assetid: 027c9ef5-4012-4d1c-b78c-a4d3f1ccbf35
title: Usar la normalización Unicode para representar cadenas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62c6d091548d924919a18fe05fb9d98d2b82b13792df2facfe96489be2d7ff2d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822495"
---
# <a name="using-unicode-normalization-to-represent-strings"></a>Usar la normalización Unicode para representar cadenas

Las aplicaciones pueden usar Unicode para representar cadenas en varios formularios. A medida que ha aumentado la aceptación de Unicode, especialmente a través de Internet, ha surgido la necesidad de eliminar las diferencias no esenciales en las cadenas Unicode. Varias representaciones para una combinación de caracteres complican el software, por ejemplo, cuando un servidor web responde a una solicitud de página o un vinculador busca un identificador determinado en una biblioteca.

> [!Caution]  
> Puede parecer que diferentes cadenas Unicode son visualmente idénticas, lo que genera problemas de seguridad. Para obtener más información, vea [Security Considerations: International Features](security-considerations--international-features.md).

 

En respuesta a este requisito, Unicode Consortium ha definido un proceso denominado "normalización", que genera una representación binaria para cualquiera de las representaciones binarias equivalentes de un carácter. Una vez normalizadas, dos cadenas son equivalentes si y solo si tienen representaciones binarias idénticas. La normalización elimina algunas diferencias, pero conserva las mayúsculas y minúsculas.

Para usar la normalización Unicode, una aplicación puede llamar a las funciones [**NormalizeString**](/windows/desktop/api/Winnls/nf-winnls-normalizestring) e [**IsNormalizedString**](/windows/desktop/api/Winnls/nf-winnls-isnormalizedstring) para reorganizar las cadenas que se ajusten a Unicode 4.0 TR \# 15. La normalización puede ayudar a mejorar la seguridad al reducir las representaciones de cadena alternativas que tienen el mismo significado lingüístico. Sin embargo, recuerde que la normalización no puede eliminar completamente las representaciones alternativas.

Para obtener una descripción detallada de los estándares Unicode para la normalización, consulte El anexo [ \# 15](https://www.unicode.org/reports/tr15) del estándar Unicode: Formularios de normalización Unicode (UAX \# 15).

> [!Caution]  
> Dado que la normalización puede cambiar la forma de una cadena, normalmente se deben implementar mecanismos de seguridad o algoritmos de validación de caracteres después de la normalización. Para obtener más información, vea [Security Considerations: International Features](security-considerations--international-features.md).

 

## <a name="provide-multiple-representations-of-the-same-string"></a>Proporcionar varias representaciones de la misma cadena

En muchos casos, Unicode permite varias representaciones de lo que es, lingüísticamente, la misma cadena. Por ejemplo:

-   El mayúscula A con diéresis (umlaut) se puede representar como un único punto de código Unicode "Ê" (U+00C4) o la combinación de Capital A y el carácter de diéresis combinado ("A" + " dín", es decir, U+0041 U+0308). Se aplican consideraciones similares para muchos otros caracteres con signos diacríticos.
-   El propio capital A se puede representar de la manera habitual (letras de capital latino A, U+0041) o de la letra A de capital latino completo (U+FF21). Se aplican consideraciones similares para las demás letras simples de latín (en mayúsculas y minúsculas) y para los caracteres katakana usados para escribir japonés.
-   La cadena "fi" se puede representar mediante los caracteres "f" e "i" (U+0066 U+0069) o mediante la ligadura "fi" (U+FB01). Se aplican consideraciones similares para muchas otras combinaciones de caracteres para las que Unicode define ligaduras.

## <a name="use-the-four-defined-normalization-forms"></a>Usar los cuatro formularios de normalización definidos

Las aplicaciones pueden realizar la normalización Unicode mediante varios algoritmos, denominados "formularios de normalización", que cumplen distintas reglas. Unicode Consortium ha definido cuatro formas de normalización: NFC (formulario C), NFD (formulario D), NFKC (formulario KC) y NFKD (formulario KD). Cada formulario elimina algunas diferencias, pero conserva las mayúsculas y minúsculas. Win32 y el .NET Framework admiten los cuatro formularios de normalización.

El tipo de enumeración [**NLS NORM \_ FORM admite**](/windows/desktop/api/Winnls/ne-winnls-norm_form) los cuatro formularios estándar de normalización Unicode. Los formularios C y D proporcionan formularios canónicos para cadenas. Las formas no canónicas KC y KD proporcionan compatibilidad adicional y pueden revelar ciertas equivalencias semánticas que no son evidentes en los formularios C y D. Sin embargo, lo hacen a costa de una pérdida determinada de información y, por lo general, no deben usarse como una manera canónica de almacenar cadenas.

De las dos formas canónicas, la forma C es una forma "compuesta" y la forma D es una forma "descompuesta". Por ejemplo, el formulario C usa el único punto de código Unicode "Ê" (U+00C4), mientras que el formulario D usa ("A" + " conversiones", es decir, U+0041 U+0308). Se representan de forma idéntica, porque "miento" (U+0308) es un carácter de combinación. El formulario D puede usar cualquier número de puntos de código para representar un único punto de código utilizado por el formulario C.

Si dos cadenas son idénticas en forma C o D, son idénticas en el otro formato. Además, cuando se representan correctamente, se muestran de forma indistinguible entre sí y de la cadena original no normalizada.

Una vez normalizadas, las cadenas no se pueden devolver de forma coherente a su representación original. Por ejemplo, si una cadena con una combinación de representaciones de caracteres compuestas y descompuestas se convierte a un formato normalizado, no hay ninguna manera de des normalizarla en la cadena mixta original. Por lo tanto, si una aplicación requiere la representación original de la cadena, debe almacenar esa representación explícitamente. Sin embargo, la conversión entre las dos formas canónicas es reversible. Una cadena con el formato C se puede convertir al formulario D y, a continuación, volver al formulario C, y el resultado es idéntico a la cadena de C del formulario original.

Los formularios KC y KD son similares a los formularios C y D, respectivamente, pero estas "formas de compatibilidad" tienen asignaciones adicionales de caracteres compatibles con la forma básica de cada carácter. Estas asignaciones pueden provocar que se pierdan variaciones de caracteres menores. Combinan determinados caracteres que son visualmente distintos. Por ejemplo, combinan caracteres de ancho completo y ancho medio con el mismo significado semántico, o diferentes formas de la misma letra árabe, o la ligadura "fi" (U+FB01) y el par de caracteres "fi" (U+0066 U+0069). También combinan algunos caracteres que a veces pueden tener un significado semántico diferente, como un dígito escrito como superíndice, como un subíndice o incluido en un círculo. Debido a esta pérdida de información, los formularios KC y KD generalmente no deben usarse como formas canónicas de cadenas, pero son útiles para determinadas aplicaciones.

Form KC es un formulario compuesto y el formato KD es un formulario descompuesto. La aplicación puede ir y volver entre formularios KC y KD, pero no hay ninguna manera coherente de pasar del formulario KC o KD a la cadena original, incluso si la cadena original está en forma C o D.

Windows, las aplicaciones de Microsoft y el .NET Framework suelen generar caracteres en forma de C mediante métodos de entrada normales. Para la mayoría de los Windows, el formulario C es el formato preferido. Por ejemplo, los caracteres con el formato C se generan mediante Windows entrada de teclado. Sin embargo, los caracteres importados desde la Web y otras plataformas pueden introducir otros formularios de normalización en el flujo de datos.

Los ejemplos siguientes se extraen de UAX 15 e ilustran las diferencias \# entre las cuatro formas de normalización.



<table>
<thead>
<tr class="header">
<th>Original</th>
<th>Formulario D</th>
<th>Formulario C</th>
<th>Notas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>&quot;Yffin&quot;</td>
<td>&quot;A\u0308ffin&quot;</td>
<td>&quot;Yffin&quot;</td>
<td rowspan="2">El ffi_ligature (U+FB03) no se descompone, porque tiene una asignación de compatibilidad, no una asignación canónica.${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>&quot;MIENTO\uFB03n&quot;</td>
<td>&quot;A\u0308\uFB03n&quot;</td>
<td>&quot;MIENTO\uFB03n&quot;</td>

</tr>
<tr class="odd">
<td>&quot;Iván IV&quot;</td>
<td>&quot;Iván IV&quot;</td>
<td>&quot;Iván IV&quot;</td>
<td rowspan="2">El IV NUMERAL DE ROMÁN (U+2163) no se descompone.${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>&quot;Enrique \u2163&quot;</td>
<td>&quot;Enrique \u2163&quot;</td>
<td>&quot;Enrique \u2163&quot;</td>

</tr>
<tr class="odd">
<td>ga</td>
<td>ka +diez</td>
<td>ga</td>
<td rowspan="5">Los distintos equivalentes de compatibilidad de un solo carácter japonés no tienen como resultado la misma cadena con el formato C.${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>ka +diez</td>
<td>ka +diez</td>
<td>ga</td>

</tr>
<tr class="odd">
<td>hw_ka +hw_ten</td>
<td>hw_ka +hw_ten</td>
<td>hw_ka +hw_ten</td>

</tr>
<tr class="even">
<td>ka +hw_ten</td>
<td>ka +hw_ten</td>
<td>ka +hw_ten</td>

</tr>
<tr class="odd">
<td>hw_ka +diez</td>
<td>hw_ka +diez</td>
<td>hw_ka +diez</td>

</tr>
<tr class="even">
<td>contrabandos</td>
<td>k <sub>i</sub> + a m + ks <sub>f</sub></td>
<td>contrabandos</td>
<td>Las sílabas hangul se mantienen en normalización.<br/></td>
</tr>
</tbody>
</table>



 



<table>
<thead>
<tr class="header">
<th>Original</th>
<th>Formulario KD</th>
<th>Formulario KC</th>
<th>Notas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>&quot;Yffin&quot;</td>
<td>&quot;A\u0308ffin&quot;</td>
<td>&quot;Yffin&quot;</td>
<td rowspan="2">El ffi_ligature (U+FB03) se descompone con el formato KC, pero no con el formato C.${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>&quot;Y\uFB03n&quot;</td>
<td>&quot;A\u0308ffin&quot;</td>
<td>&quot;Yffin&quot;</td>

</tr>
<tr class="odd">
<td>&quot;Iván&quot;</td>
<td>&quot;Iván&quot;</td>
<td>&quot;Iván&quot;</td>
<td rowspan="2">Las cadenas resultantes aquí son idénticas en el formato KC.${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>&quot;Quería \u2163&quot;</td>
<td>&quot;Iván&quot;</td>
<td>&quot;Iván&quot;</td>

</tr>
<tr class="odd">
<td>ga</td>
<td>ka +diez</td>
<td>ga</td>
<td rowspan="5">Los distintos equivalentes de compatibilidad de un único carácter japonés tienen como resultado la misma cadena con el formato KC.${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>ka +diez</td>
<td>ka +diez</td>
<td>ga</td>

</tr>
<tr class="odd">
<td>hw_ka +hw_ten</td>
<td>ka +diez</td>
<td>ga</td>

</tr>
<tr class="even">
<td>ka +hw_ten</td>
<td>ka +diez</td>
<td>ga</td>

</tr>
<tr class="odd">
<td>hw_ka +diez</td>
<td>ka +diez</td>
<td>ga</td>

</tr>
<tr class="even">
<td>contrabandos</td>
<td>k <sub>i</sub> + a m + ks <sub>f</sub></td>
<td>contrabandos</td>
<td>Las sílabas hangul se mantienen en normalización. En versiones anteriores de Unicode, los caracteres jamo como ks <sub>f</sub> tenían asignaciones de compatibilidad a k <sub>f</sub> + s <sub>f</sub>. Estas asignaciones se quitaron en Unicode 2.1.9 para asegurarse de que se mantienen las sílabas de Hangul.<br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Las dos tablas anteriores tienen un copyright de © Unicode, Inc. 1998-2006. Todos los derechos reservados.

 

## <a name="use-composed-forms-for-single-glyphs"></a>Usar formularios compuestos para glifos únicos

Muchas secuencias de caracteres que corresponden a un único glifo no tienen formas compuestas. Incluso cuando se normaliza con el formato C, un único glifo visual o elemento de texto lógico puede estar compuesto de varios puntos de código Unicode. Por ejemplo, varios caracteres que se usan para escribir El lituano tienen signos diacríticos dobles, ya que solo tienen formas descompuestas. Un ejemplo es la minúscula U con macron y tilde ("miento", U+016b U+0303, donde el primer punto de código es una U minúscula con macron y el segundo es una combinación de acentos acentuado).

## <a name="example"></a>Ejemplo

Puede encontrar un ejemplo relevante en [NLS: Ejemplo de normalización Unicode](nls--unicode-normalization-sample.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de la compatibilidad con idiomas nacionales](using-national-language-support.md)
</dt> <dt>

[Consideraciones de seguridad: Características internacionales](security-considerations--international-features.md)
</dt> <dt>

[**IsNormalizedString**](/windows/desktop/api/Winnls/nf-winnls-isnormalizedstring)
</dt> <dt>

[**NormalizeString**](/windows/desktop/api/Winnls/nf-winnls-normalizestring)
</dt> </dl>

 

 




