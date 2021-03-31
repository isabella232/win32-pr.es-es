---
description: En este tema se proporcionan procedimientos recomendados y sugerencias para validar y solucionar problemas de las implementaciones de IWordBreaker y IStemmer.
ms.assetid: b0e199b9-8d81-4445-92f7-de9b8a00a9cb
title: Solución de problemas de recursos de lenguaje y procedimientos recomendados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f63a0a8acda3fff1627b37f41c2d81a67b37d66a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808888"
---
# <a name="troubleshooting-language-resources-and-best-practices"></a>Solución de problemas de recursos de lenguaje y procedimientos recomendados

En este tema se proporcionan procedimientos recomendados y sugerencias para validar y solucionar problemas de las implementaciones de [**IWordBreaker**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordbreaker) y [**IStemmer**](/windows/desktop/api/Indexsrv/nn-indexsrv-istemmer) .

Este tema se organiza de la siguiente manera:

-   [Procedimientos recomendados](#best-practices)
-   [Prueba de la coherencia de analizador lingüístico](#testing-stemmer-consistency)
-   [Prueba de la entrada no válida en el analizador lingüístico](#testing-for-invalid-input-in-the-stemmer)
-   [Probar la coherencia del separador de palabras](#testing-word-breaker-consistency)
-   [Prueba de una entrada no válida en el separador de palabras](#testing-for-invalid-input-in-the-word-breaker)

### <a name="best-practices"></a>Prácticas recomendadas

-   Asegúrese de que el modelo de subprocesos para los recursos de idioma está establecido en "ambos" en el registro.
-   Siempre que sea posible, coloque los datos de idioma en un recurso de la DLL en lugar de en un archivo independiente. Esto hace que la DLL sea más fácil de instalar y más segura. Además, si se colocan datos de idioma en un recurso, se mejorará el rendimiento de ese componente de recurso de idioma.
-   Minimice los recursos del sistema que usan los componentes de recursos de idioma. Por ejemplo, si cada instancia de un objeto de recurso de lenguaje necesita acceso de solo lectura a un léxico, considere la posibilidad de compartir el léxico en todas las instancias.
-   Considere la posibilidad de usar el separador de palabras neutro para controlar el texto que no está en el idioma o la configuración regional de la implementación del separador de palabras. Esto le ayudará a garantizar que el texto se procesa de forma coherente en todos los lenguajes.
-   Compruebe todos los códigos de retorno y devuelvalos desde funciones como [**IStemmer:: GenerateWordForms**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-generatewordforms) y [**IWordBreaker:: BreakText**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext). Si se produce un error en la indización, es importante pasar el error para que se notifique al usuario qué documentos se indexaron.

### <a name="testing-stemmer-consistency"></a>Prueba de la coherencia de analizador lingüístico

Se recomienda supervisar el rendimiento de una implementación de [**IStemmer**](/windows/desktop/api/Indexsrv/nn-indexsrv-istemmer) para mantener la coherencia en las siguientes condiciones:

-   El analizador lingüístico se comporta de forma coherente en varias llamadas a [**IStemmer:: init**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-init). El analizador lingüístico se reinicializa con los mismos parámetros que en la inicialización anterior, sin liberar los parámetros.
-   Dado el mismo corpus de pruebas y las repeticiones de la misma consulta, [**IStemmer:: GenerateWordForms**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-generatewordforms) genera el resultado idéntico y realiza llamadas idénticas a los métodos del objeto [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) .

### <a name="testing-for-invalid-input-in-the-stemmer"></a>Prueba de la entrada no válida en el analizador lingüístico

Se recomienda supervisar el modo en que los métodos [**IStemmer**](/windows/desktop/api/Indexsrv/nn-indexsrv-istemmer) controlan todos los errores relacionados con los parámetros no válidos. Además, se recomienda asegurarse de que los métodos lingüísticos no generan excepciones no controladas. El analizador lingüístico debe controlar los errores siguientes:

-   Llame a [**IStemmer:: init**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-init) con *PfLicense* establecido en **null**. Init genera un error y no produce una infracción de acceso.
-   Llame a [**IStemmer:: GetLicenseToUse**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-getlicensetouse) con el parámetro *PpwcsLicense* establecido en **null**. **IStemmer:: GetLicenseToUse** no produce una infracción de acceso.
-   Llame a [**IStemmer:: GenerateWordForms**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-generatewordforms) con el parámetro *PwcInBuf* establecido en **null**. **IStemmer:: GenerateWordForms** produce un error (devuelve E \_ Fail) y no produce una infracción de acceso.
-   Llame a [**IStemmer:: GenerateWordForms**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-generatewordforms) con el parámetro *CWC* igual a 0. **IStemmer:: GenerateWordForms** devuelve correctamente (devuelve S \_ OK) y no produce una infracción de acceso.
-   Llame a [**IStemmer:: GenerateWordForms**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-generatewordforms) con el parámetro *PwcInBuf* establecido en **null** y el parámetro *CWC* igual a 0. **IStemmer:: GenerateWordForms** produce un error (devuelve E \_ Fail) y no produce una infracción de acceso.

### <a name="testing-word-breaker-consistency"></a>Probar la coherencia del separador de palabras

Se recomienda asegurarse de que la implementación de [**IWordBreaker**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordbreaker) se realiza de forma coherente en las siguientes condiciones:

-   El separador de palabras se realiza de forma coherente en varias llamadas a su método [**IWordBreaker:: init**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-init) . El separador de palabras se reinicializa con los mismos parámetros que en la inicialización anterior, sin liberar los parámetros.
-   Dado el mismo corpus de pruebas y las repeticiones de la misma consulta, el método [**IWordBreaker:: BreakText**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext) genera el resultado idéntico y realiza llamadas idénticas a los métodos de los objetos [**IWordSink**](iwordsink.md) y [**IPhraseSink**](/windows/win32/api/indexsrv/nn-indexsrv-iphrasesink) .

### <a name="testing-for-invalid-input-in-the-word-breaker"></a>Prueba de una entrada no válida en el separador de palabras

Se recomienda asegurarse de que los métodos de [**IWordBreaker**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordbreaker) controlen todos los errores relacionados con los parámetros no válidos. Además, se recomienda asegurarse de que los métodos del separador de palabras no produzcan excepciones no controladas. El separador de palabras debe realizar las siguientes funciones y controlar los errores siguientes:

-   La llamada a [**IWordBreaker:: init**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-init) debe devolver una base de datos de idioma que \_ \_ \_ no \_ se encuentre o que sea \_ correcta.
-   La llamada a [**IWordBreaker:: init**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-init) inicializa correctamente el parámetro *pfLicense* en **false** y llama a [**IStemmer:: GetLicenseToUse**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-getlicensetouse) y no produce una infracción de acceso.
-   El separador de palabras no lee más allá del final del parámetro *awcBuffer* en el método [**IWordBreaker:: BreakText**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext) .
-   Llame a [**IWordBreaker:: BreakText**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext) con *PwcInBuf* establecido en **null**. **IWordBreaker:: BreakText** produce un error (devuelve E \_ Fail) y no produce una infracción de acceso.
-   Llame a [**IWordBreaker:: BreakText**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext) con el parámetro *CWC* igual a 0. **IWordBreaker:: BreakText** devuelve correctamente (devuelve S \_ OK) y no produce una infracción de acceso.
-   Llame al método [**IWordBreaker:: BreakText**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext) con el parámetro *PwcInBuf* establecido en **null** y el parámetro *CWC* igual a 0. **IWordBreaker:: BreakText** produce un error (devuelve E \_ Fail) y no produce una infracción de acceso.
-   Las frases generadas durante la creación del índice contienen el mismo número de palabras.
-   Las frases se generan durante la creación del índice mediante llamadas sucesivas a los métodos [**IWordFormSink::P utword**](iwordsink-putword.md) y [**IWordFormSink::P utaltword**](iwordsink-putaltword.md) . El separador de palabras solo usa el objeto [**IPhraseSink**](/windows/win32/api/indexsrv/nn-indexsrv-iphrasesink) durante el tiempo de consulta.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Extensión de recursos de idioma](extending-language-resources-in-windows-search.md)
</dt> <dt>

[Descripción de los componentes de recursos de lenguaje](understanding-language-resource-components.md)
</dt> <dt>

[Implementar un separador de palabras y un analizador lingüístico](implementing-a-word-breaker-and-stemmer.md)
</dt> <dt>

[Consideraciones lingüísticas y Unicode](linguistic-and-unicode-considerations.md)
</dt> </dl>

 

 
