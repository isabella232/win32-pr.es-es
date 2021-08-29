---
description: En este tema se proporcionan procedimientos recomendados y sugerencias para validar y solucionar problemas de las implementaciones de IWordBreaker e IStemmer.
ms.assetid: b0e199b9-8d81-4445-92f7-de9b8a00a9cb
title: Solución de problemas de recursos de lenguaje y procedimientos recomendados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8704597f88bdf77e301dcf3f2099c27ad85eae656e3acdcbd6e43c134bb7e43
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119844495"
---
# <a name="troubleshooting-language-resources-and-best-practices"></a>Solución de problemas de recursos de lenguaje y procedimientos recomendados

En este tema se proporcionan procedimientos recomendados y sugerencias para validar y solucionar problemas de las implementaciones [**de IWordBreaker**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordbreaker) [**e IStemmer.**](/windows/desktop/api/Indexsrv/nn-indexsrv-istemmer)

Este tema se organiza de la siguiente manera:

-   [Procedimientos recomendados](#best-practices)
-   [Probar la coherencia del lematizador](#testing-stemmer-consistency)
-   [Prueba de una entrada no válida en el lematizador](#testing-for-invalid-input-in-the-stemmer)
-   [Probar la coherencia del separador de palabras](#testing-word-breaker-consistency)
-   [Prueba de entrada no válida en el separador de palabras](#testing-for-invalid-input-in-the-word-breaker)

### <a name="best-practices"></a>Procedimientos recomendados

-   Asegúrese de que el modelo de subprocesos para los recursos de lenguaje está establecido en "ambos" en el Registro.
-   Siempre que sea posible, coloque los datos de lenguaje en un recurso del archivo DLL en lugar de en un archivo independiente. Esto hace que el archivo DLL sea más fácil de instalar y más seguro. Además, la colocación de datos de idioma en un recurso dará como resultado un rendimiento mejorado para ese componente de recursos de lenguaje.
-   Minimice los recursos del sistema que usan los componentes de recursos de lenguaje. Por ejemplo, si cada instancia de un objeto de recurso de lenguaje necesita acceso de solo lectura a un léxico, considere la posibilidad de compartir el léxico entre todas las instancias.
-   Considere la posibilidad de usar el separador de palabras neutro para controlar el texto que no está en el idioma o la configuración regional de la implementación del separador de palabras. Esto ayudará a garantizar que el texto se procese de forma coherente en todos los idiomas.
-   Compruebe todos los códigos de retorno y devolución de funciones como [**IStemmer::GenerateWordForms**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-generatewordforms) e [**IWordBreaker::BreakText**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext). Si se produce un error en la indexación, es importante pasar el error para que se notifique al usuario qué documentos se indexan.

### <a name="testing-stemmer-consistency"></a>Probar la coherencia del lematizador

Se recomienda supervisar el rendimiento de una implementación de [**IStemmer**](/windows/desktop/api/Indexsrv/nn-indexsrv-istemmer) para mantener la coherencia en las condiciones siguientes:

-   El lematizador realiza un rendimiento coherente en varias llamadas a [**IStemmer::Init**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-init). El lematizador reinicializa con los mismos parámetros que en la inicialización anterior, sin liberar los parámetros.
-   Dado el mismo corpus de prueba y las repeticiones de la misma consulta, [**IStemmer::GenerateWordForms**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-generatewordforms) genera la salida idéntica y realiza llamadas idénticas a los métodos del objeto [**IWordFormSink.**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink)

### <a name="testing-for-invalid-input-in-the-stemmer"></a>Prueba de una entrada no válida en el lematizador

Se recomienda supervisar cómo los métodos [**de IStemmer**](/windows/desktop/api/Indexsrv/nn-indexsrv-istemmer) controlan todos los errores relacionados con parámetros no válidos. Además, se recomienda asegurarse de que los métodos de lematizador no generen excepciones no controladas. El lematizador debe controlar los errores siguientes:

-   Llame a [**IStemmer::Init**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-init) con *pfLicense* establecido en **NULL.** Init produce un error y no produce una infracción de acceso.
-   Llame a [**IStemmer::GetLicenseToUse con**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-getlicensetouse) el *parámetro ppwcsLicense* establecido en **NULL.** **IStemmer::GetLicenseToUse** no da lugar a una infracción de acceso.
-   Llame a [**IStemmer::GenerateWordForms**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-generatewordforms) con el parámetro *pwcInBuf* establecido en **NULL.** Se produce un error en **IStemmer::GenerateWordForms** (devuelve E FAIL) y no \_ produce una infracción de acceso.
-   Llame a [**IStemmer::GenerateWordForms**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-generatewordforms) con el *parámetro cwc* igual a 0. **IStemmer::GenerateWordForms** devuelve correctamente (devuelve S OK) y no \_ produce una infracción de acceso.
-   Llame a [**IStemmer::GenerateWordForms**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-generatewordforms) con el parámetro *pwcInBuf* establecido en **NULL** y el *parámetro cwc* igual a 0. Se produce un error en **IStemmer::GenerateWordForms** (devuelve E FAIL) y no \_ produce una infracción de acceso.

### <a name="testing-word-breaker-consistency"></a>Probar la coherencia del separador de palabras

Se recomienda asegurarse de que la implementación [**de IWordBreaker**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordbreaker) funciona de forma coherente en las condiciones siguientes:

-   El separador de palabras funciona de forma coherente en varias llamadas a su [**método IWordBreaker::Init.**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-init) El separador de palabras reinicializa con los mismos parámetros que en la inicialización anterior, sin liberar los parámetros.
-   Dado el mismo corpus de prueba y las repeticiones de la misma consulta, el método [**IWordBreaker::BreakText**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext) genera la salida idéntica y realiza llamadas idénticas a los métodos de los objetos [**IWordSink**](iwordsink.md) e [**IPhraseSink.**](/windows/win32/api/indexsrv/nn-indexsrv-iphrasesink)

### <a name="testing-for-invalid-input-in-the-word-breaker"></a>Prueba de entrada no válida en el separador de palabras

Se recomienda asegurarse de que los métodos [**IWordBreaker**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordbreaker) controlan todos los errores relacionados con parámetros no válidos. Además, se recomienda asegurarse de que los métodos de separador de palabras no generen excepciones no controladas. El separador de palabras debe realizar las siguientes funciones y controlar los errores siguientes:

-   La llamada [**a IWordBreaker::Init**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-init) debe devolver LANGUAGE \_ E DATABASE NOT FOUND o S \_ \_ \_ \_ OK.
-   La llamada a [**IWordBreaker::Init**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-init) inicializa correctamente el parámetro *pfLicense* en **FALSE** y llama a [**IStemmer::GetLicenseToUse**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-getlicensetouse) y no da lugar a una infracción de acceso.
-   El separador de palabras no lee más allá del final del parámetro *awcBuffer* en el [**método IWordBreaker::BreakText.**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext)
-   Llame a [**IWordBreaker::BreakText**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext) con *pwcInBuf* establecido en **NULL.** **IWordBreaker::BreakText** produce un error (devuelve E FAIL) y \_ no produce una infracción de acceso.
-   Llame a [**IWordBreaker::BreakText**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext) con el *parámetro cwc* igual a 0. **IWordBreaker::BreakText** devuelve correctamente (devuelve S OK) y no da lugar \_ a una infracción de acceso.
-   Llame al [**método IWordBreaker::BreakText**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext) con el parámetro *pwcInBuf* establecido en **NULL** y el *parámetro cwc* igual a 0. **IWordBreaker::BreakText** produce un error (devuelve E FAIL) y \_ no produce una infracción de acceso.
-   Las frases generadas durante la creación del índice contienen el mismo número de palabras.
-   Las frases se generan durante la creación del índice mediante llamadas sucesivas a los métodos [**IWordFormSink::P utWord**](iwordsink-putword.md) e [**IWordFormSink::P utAltWord.**](iwordsink-putaltword.md) El separador de palabras solo usa [**el objeto IPhraseSink**](/windows/win32/api/indexsrv/nn-indexsrv-iphrasesink) durante el tiempo de consulta.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Extensión de recursos de lenguaje](extending-language-resources-in-windows-search.md)
</dt> <dt>

[Descripción de los componentes de recursos de lenguaje](understanding-language-resource-components.md)
</dt> <dt>

[Implementar un separador de palabras y un lematizador](implementing-a-word-breaker-and-stemmer.md)
</dt> <dt>

[Consideraciones lingüísticas y Unicode](linguistic-and-unicode-considerations.md)
</dt> </dl>

 

 
