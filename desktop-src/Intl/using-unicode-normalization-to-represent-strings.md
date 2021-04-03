---
description: Las aplicaciones pueden utilizar Unicode para representar cadenas en varios formatos.
ms.assetid: 027c9ef5-4012-4d1c-b78c-a4d3f1ccbf35
title: Usar la normalización Unicode para representar cadenas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad452db3bc20518320afcf77e5f6483e010cd144
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913690"
---
# <a name="using-unicode-normalization-to-represent-strings"></a>Usar la normalización Unicode para representar cadenas

Las aplicaciones pueden utilizar Unicode para representar cadenas en varios formatos. Como la aceptación de Unicode ha crecido, especialmente a través de Internet, la necesidad ha surgido para eliminar las diferencias no esenciales en las cadenas Unicode. Varias representaciones para una combinación de caracteres complican el software, por ejemplo, cuando un servidor web responde a una solicitud de página o un vinculador busca un identificador determinado en una biblioteca.

> [!Caution]  
> Puede parecer que las distintas cadenas Unicode son visualmente idénticas, lo que plantea problemas de seguridad. Para obtener más información, vea [consideraciones de seguridad: características internacionales](security-considerations--international-features.md).

 

En respuesta a este requisito, el consorcio Unicode ha definido un proceso denominado "normalización", que genera una representación binaria para cualquiera de las representaciones binarias equivalentes de un carácter. Una vez normalizada, dos cadenas son equivalentes si y solo si tienen representaciones binarias idénticas. La normalización elimina algunas diferencias, pero conserva el uso de mayúsculas y minúsculas.

Para usar la normalización Unicode, una aplicación puede llamar a las funciones [**NormalizeString**](/windows/desktop/api/Winnls/nf-winnls-normalizestring) y [**IsNormalizedString**](/windows/desktop/api/Winnls/nf-winnls-isnormalizedstring) para reorganizar las cadenas acccording a Unicode 4,0 TR \# 15. La normalización puede ayudar a mejorar la seguridad al reducir las representaciones de cadena alternativas que tienen el mismo significado lingüístico. No obstante, recuerde que la normalización no puede eliminar completamente las representaciones alternativas.

Para obtener una descripción detallada de los estándares Unicode para la normalización, consulte el [Anexo 15 del estándar Unicode ( \# formas de normalización de Unicode](https://www.unicode.org/reports/tr15) ) (UAX \# 15).

> [!Caution]  
> Dado que la normalización puede cambiar la forma de una cadena, los mecanismos de seguridad o los algoritmos de validación de caracteres deben implementarse normalmente después de la normalización. Para obtener más información, vea [consideraciones de seguridad: características internacionales](security-considerations--international-features.md).

 

## <a name="provide-multiple-representations-of-the-same-string"></a>Proporcionar varias representaciones de la misma cadena

En muchos casos, Unicode permite varias representaciones de lo que es, lingüísticamente, la misma cadena. Por ejemplo:

-   La mayúscula A con el diéresis (diéresis) se puede representar como un único punto de código Unicode "Ä" (U + 00C4) o la combinación de mayúsculas A y el carácter de diéresis de combinación ("A" + "̈", es decir, U + 0041 U + 0308). Las consideraciones similares se aplican a muchos otros caracteres con marcas diacríticas.
-   Un solo se puede representar de la manera habitual (letra mayúscula latina A, U + 0041) o por la letra mayúscula latina de ancho completo A (U + FF21). Se aplican consideraciones similares para las demás letras latinas simples (mayúsculas y minúsculas) y para los caracteres katakana usados en la escritura en japonés.
-   La cadena "fi" se puede representar mediante los caracteres "f" y "i" (U + 0066 U + 0069) o por la ligadura "fi" (U + FB01). Se aplican consideraciones similares para muchas otras combinaciones de caracteres para los que Unicode define las ligaduras.

## <a name="use-the-four-defined-normalization-forms"></a>Usar las cuatro formas de normalización definidas

Las aplicaciones pueden realizar la normalización Unicode mediante varios algoritmos, denominados "formas de normalización", que obedecen las distintas reglas. Unicode Consortium ha definido cuatro formas de normalización: NFC (formulario C), NFD (formulario D), NFKC (formulario KC) y NFKD (Form KD). Cada formulario elimina algunas diferencias, pero conserva el uso de mayúsculas y minúsculas. Win32 y el .NET Framework admiten las cuatro formas de normalización.

La [**\_ forma**](/windows/desktop/api/Winnls/ne-winnls-norm_form) de tipo de enumeración NLS es compatible con las cuatro formas estándar de normalización Unicode. Los formularios C y D proporcionan formas canónicas para las cadenas. Los formularios no canónicos KC y KD proporcionan compatibilidad adicional y pueden revelar ciertas equivalencias semánticas que no son aparentes en los formularios C y D. Sin embargo, lo hacen a costa de una determinada pérdida de información y, por lo general, no deben usarse como una manera canónica de almacenar cadenas.

De las dos formas canónicas, el formulario C es un formulario "compuesto" y un formulario D es un formulario "descompuesto". Por ejemplo, el formulario C usa el punto de código Unicode "Ä" (U + 00C4), mientras que el formulario D USA ("A" + "̈", que es U + 0041 U + 0308). Se representan de forma idéntica, ya que "̈" (U + 0308) es un carácter de combinación. El formato D puede usar cualquier número de puntos de código para representar un punto de código único utilizado por el formulario C.

Si dos cadenas son idénticas en el formulario C o en el formulario D, son idénticas en el otro formulario. Además, cuando se representa correctamente, se muestran indistinguidamente entre sí y desde la cadena no normalizada original.

Una vez normalizadas, las cadenas no se pueden devolver de forma coherente a su representación original. Por ejemplo, si una cadena con una mezcla de representaciones de caracteres compuestas y descompuestas se convierte en un formato normalizado, no hay ninguna manera de anular la normalización de la cadena mixta original. Por lo tanto, si una aplicación requiere la representación original de la cadena, debe almacenar esa representación explícitamente. Sin embargo, la conversión entre las dos formas canónicas es reversible. Una cadena del formulario C se puede convertir al formato D y después volver al formulario C, y el resultado es idéntico a la cadena de C del formulario original.

Los formularios KC y KD son similares a los formularios C y D, respectivamente, pero estos "formularios de compatibilidad" tienen asignaciones adicionales de caracteres compatibles con el formato básico de cada carácter. Estas asignaciones pueden provocar que se pierdan variaciones de caracteres menores. Combinan ciertos caracteres que son visualmente distintos. Por ejemplo, combinan caracteres de ancho completo y de ancho medio con el mismo significado semántico, o con distintas formas de la misma letra árabe, o la ligadura "fi" (U + FB01) y el par de caracteres "fi" (U + 0066 U + 0069). También combinan algunos caracteres que a veces pueden tener un significado semántico diferente, como un dígito escrito como superíndice, como un subíndice, o incluido en un círculo. Debido a esta pérdida de información, los formularios KC y KD generalmente no deben usarse como formas canónicas de cadenas, pero son útiles para determinadas aplicaciones.

El formulario KC es un formulario compuesto y el formulario KD es un formulario descompuesto. La aplicación puede avanzar y retroceder entre los formularios KC y KD, pero no hay ninguna manera coherente de pasar del formulario KC o KD a la cadena original, incluso si la cadena original está en la forma C o D.

Windows, las aplicaciones de Microsoft y el .NET Framework generalmente generan caracteres en el formulario C mediante métodos de entrada normales. Para la mayoría de los propósitos de Windows, el formulario C es la forma preferida. Por ejemplo, los caracteres del formulario C se generan mediante la entrada del teclado de Windows. Sin embargo, los caracteres importados desde la web y otras plataformas pueden introducir otras formas de normalización en el flujo de datos.

Los ejemplos siguientes se extraen de UAX \# 15 y muestran las diferencias entre las cuatro formas de normalización.



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
<td>&quot;Äffin&quot;</td>
<td>&quot;A\u0308ffin&quot;</td>
<td>&quot;Äffin&quot;</td>
<td rowspan="2">El ffi_ligature (U + FB03) no se descompone porque tiene una asignación de compatibilidad, no una asignación canónica. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>&quot;Ä \ uFB03n&quot;</td>
<td>&quot;A\u0308\uFB03n&quot;</td>
<td>&quot;Ä \ uFB03n&quot;</td>

</tr>
<tr class="odd">
<td>&quot;Henry IV&quot;</td>
<td>&quot;Henry IV&quot;</td>
<td>&quot;Henry IV&quot;</td>
<td rowspan="2">El número romano IV (U + 2163) no se descompone. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>&quot;Henry \u2163&quot;</td>
<td>&quot;Henry \u2163&quot;</td>
<td>&quot;Henry \u2163&quot;</td>

</tr>
<tr class="odd">
<td>ga</td>
<td>Ka + diez</td>
<td>ga</td>
<td rowspan="5">Los diferentes equivalentes de compatibilidad de un solo carácter japonés no dan como resultado la misma cadena de la forma C. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>Ka + diez</td>
<td>Ka + diez</td>
<td>ga</td>

</tr>
<tr class="odd">
<td>hw_ka + hw_ten</td>
<td>hw_ka + hw_ten</td>
<td>hw_ka + hw_ten</td>

</tr>
<tr class="even">
<td>Ka + hw_ten</td>
<td>Ka + hw_ten</td>
<td>Ka + hw_ten</td>

</tr>
<tr class="odd">
<td>hw_ka + diez</td>
<td>hw_ka + diez</td>
<td>hw_ka + diez</td>

</tr>
<tr class="even">
<td>kaks</td>
<td>k <sub>i</sub> + a m + KS <sub>f</sub></td>
<td>kaks</td>
<td>Las sílabas hangul se mantienen en la normalización.<br/></td>
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
<td>&quot;Äffin&quot;</td>
<td>&quot;A\u0308ffin&quot;</td>
<td>&quot;Äffin&quot;</td>
<td rowspan="2">El ffi_ligature (U + FB03) se descompone en el formulario KC, pero no en el formulario C. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>&quot;Ä \ uFB03n&quot;</td>
<td>&quot;A\u0308ffin&quot;</td>
<td>&quot;Äffin&quot;</td>

</tr>
<tr class="odd">
<td>&quot;Henry IV&quot;</td>
<td>&quot;Henry IV&quot;</td>
<td>&quot;Henry IV&quot;</td>
<td rowspan="2">Las cadenas resultantes son idénticas en el formulario KC. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>&quot;Henry \u2163&quot;</td>
<td>&quot;Henry IV&quot;</td>
<td>&quot;Henry IV&quot;</td>

</tr>
<tr class="odd">
<td>ga</td>
<td>Ka + diez</td>
<td>ga</td>
<td rowspan="5">Los diferentes equivalentes de compatibilidad de un solo carácter japonés dan como resultado la misma cadena en el formulario KC. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>Ka + diez</td>
<td>Ka + diez</td>
<td>ga</td>

</tr>
<tr class="odd">
<td>hw_ka + hw_ten</td>
<td>Ka + diez</td>
<td>ga</td>

</tr>
<tr class="even">
<td>Ka + hw_ten</td>
<td>Ka + diez</td>
<td>ga</td>

</tr>
<tr class="odd">
<td>hw_ka + diez</td>
<td>Ka + diez</td>
<td>ga</td>

</tr>
<tr class="even">
<td>kaks</td>
<td>k <sub>i</sub> + a m + KS <sub>f</sub></td>
<td>kaks</td>
<td>Las sílabas hangul se mantienen en la normalización. En versiones anteriores de Unicode, los caracteres Jamo como KS <sub>f</sub> tenían asignaciones de compatibilidad a k <sub>f</sub> + s. <sub></sub> Estas asignaciones se quitaron en Unicode 2.1.9 para asegurarse de que se mantienen las sílabas hangul.<br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Las dos tablas anteriores tienen un copyright de © 1998-2006 Unicode, Inc. Todos los derechos reservados.

 

## <a name="use-composed-forms-for-single-glyphs"></a>Usar formularios compuestos para glifos únicos

Muchas secuencias de caracteres que corresponden a un solo glifo no tienen formas compuestas. Incluso cuando se normaliza con el formulario C, un solo glifo visual o elemento de texto lógico pueden estar compuestos de varios puntos de código Unicode. Por ejemplo, varios caracteres usados al escribir Lituano tienen signos de dos dobles, ya que solo tienen formularios descompuestos. Un ejemplo es una U minúscula con Macron y tildes ("ū̃", U + 016B U + 0303, donde el primer punto de código es una U minúscula con Macron y el segundo es un acento agudo de combinación).

## <a name="example"></a>Ejemplo

Un ejemplo relevante puede encontrarse en [NLS: ejemplo de normalización Unicode](nls--unicode-normalization-sample.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de la compatibilidad con National Language](using-national-language-support.md)
</dt> <dt>

[Consideraciones de seguridad: características internacionales](security-considerations--international-features.md)
</dt> <dt>

[**IsNormalizedString**](/windows/desktop/api/Winnls/nf-winnls-isnormalizedstring)
</dt> <dt>

[**NormalizeString**](/windows/desktop/api/Winnls/nf-winnls-normalizestring)
</dt> </dl>

 

 




