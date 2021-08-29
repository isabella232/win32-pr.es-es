---
description: Se hace referencia a un reconocedor de lápiz con un identificador HRECOGNIZER y un contexto de reconocedor como identificador HRECOCONTEXT. Una biblioteca de vínculos dinámicos (DLL) de reconocedor puede implementar reconocedores para más de un idioma.
ms.assetid: 23002d02-cf8f-489b-a50f-4a18ac091825
title: HRECOGNIZER y HRECOCONTEXT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ea6f9f4facae72186d1faba09b3e7d9d667983fea92b8397f53d5896d7de298
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119597215"
---
# <a name="hrecognizer-and-hrecocontext"></a>HRECOGNIZER y HRECOCONTEXT

Se hace referencia a un reconocedor de lápiz con un identificador [HRECOGNIZER](hrecognizer-handle.md) y un contexto de reconocedor como [identificador HRECOCONTEXT.](hrecocontext-handle.md)

Una biblioteca de vínculos dinámicos (DLL) de reconocedor puede implementar reconocedores para más de un idioma. Si es así, cada idioma se selecciona mediante un CLSID que se pasa al crear el objeto [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) en la aplicación. Además, un archivo DLL de reconocedor puede crear varios identificadores de reconocedor cuando se carga, uno o varios para cada idioma reconocido.

Se crea un contexto de reconocedor para representar el evento de reconocer un fragmento de lápiz específico. Cuando se crea el contexto, el identificador de objetos de reconocedor asociado se pasa a la [**función CreateContext.**](/windows/desktop/api/recapis/nf-recapis-createcontext) Esto asocia el lenguaje al contexto del reconocedor.

Un contexto de reconocedor puede representar el reconocimiento de toda la entrada de lápiz en el cuerpo de un correo electrónico, la entrada de lápiz de un solo campo dentro de una aplicación o una sola línea de texto escrita en el panel de entrada de Tablet PC. El volumen de lápiz en un único contexto de reconocedor puede variar de un solo trazo a una página completa o más.

El contexto del reconocedor se define mediante la configuración de:

-   Guía de reconocimiento.
-   Cualquier factoids.
-   Cualquier marca.
-   Contexto de texto.
-   Cualquier lista de palabras.
-   El modo autocompletar del carácter.

El identificador del contexto del reconocedor se pasa a todas las funciones que usan esta configuración. Al cambiar una configuración, se cambia el contexto del reconocedor.

La aplicación puede usar varios contextos para reconocer la entrada de lápiz de diferentes partes de la pantalla. Un contexto individual puede reconocer varias líneas de texto. Sin embargo, un contexto individual no puede procesar dos párrafos escritos en paralelo, como varias columnas en un artículo de periódico.

Para reconocer la entrada de lápiz nueva, cree un contexto. Como alternativa, use la función [**CloneContext**](/windows/desktop/api/recapis/nf-recapis-clonecontext) para realizar una copia de un contexto que no tenga la entrada de lápiz y los resultados, o bien la función [**ResetContext**](/windows/desktop/api/recapis/nf-recapis-resetcontext) para borrar un contexto de la entrada de lápiz y los resultados. Con estos enfoques, una aplicación de entrada de lápiz puede reutilizar un contexto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**SetGuide (Función)**](/windows/desktop/api/recapis/nf-recapis-setguide)
</dt> <dt>

[**GetGuide (Función)**](/windows/desktop/api/recapis/nf-recapis-getguide)
</dt> <dt>

[**SetFactoid (Función)**](/windows/desktop/api/recapis/nf-recapis-setfactoid)
</dt> <dt>

[**SetFlags (Función)**](/windows/desktop/api/recapis/nf-recapis-setflags)
</dt> <dt>

[**SetEnabledUnicodeRanges (Función)**](/windows/desktop/api/recapis/nf-recapis-setenabledunicoderanges)
</dt> <dt>

[**GetEnabledUnicodeRanges (Función)**](/windows/desktop/api/recapis/nf-recapis-getenabledunicoderanges)
</dt> <dt>

[**SetCACMode (Función)**](/windows/desktop/api/recapis/nf-recapis-setcacmode)
</dt> <dt>

[**SetTextContext (Función)**](/windows/desktop/api/recapis/nf-recapis-settextcontext)
</dt> <dt>

[**SetWordList (Función)**](/windows/desktop/api/recapis/nf-recapis-setwordlist)
</dt> </dl>

 

 



