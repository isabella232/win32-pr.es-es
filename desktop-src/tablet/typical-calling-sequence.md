---
description: 'Las API de la plataforma de Tablet PC llaman a los métodos que debe implementar para crear un reconocedor de entrada de lápiz y no directamente a una aplicación habilitada para lápiz. Los pasos siguientes representan una secuencia de llamada típica para la implementación de estos métodos: se carga el archivo DLL. Un&\# 160; Se crea el identificador HRECOGNIZER. Un&\# 160; Se crea el identificador HRECOCONTEXT. Las opciones y los modos del reconocedor se establecen para este contexto. Los trazos se agregan a los datos de entrada de lápiz. La entrada ha finalizado. Se reconoce la entrada de lápiz. Se devuelven los resultados del reconocimiento. Se destruye el identificador HRECOCONTEXT. Se destruye el identificador HRECOGNIZER. La secuencia de llamada también se muestra en el siguiente esquema de código: C++CreateRecognizer(CLSID, &hrec); while (más piezas de lápiz para reconocer ... ) { // Cree un contexto, una vez por fragmento de lápiz para que se reconozca hrc = CreateContext(hrec, &hrc); // Funciones para configurar opciones y modos para este contexto SetGuide(hrc, pGuide, 0); SetFactoid(hrc, 5, PHONE); solo si en la aplicación con formularios SetFlags(hrc, RECOFLAG WORDMODE); // rare, solo si se desea el modo de palabra, sin falta de diccionario o una segmentación única SetWordList(hrc, hwl); // Agregar todos los trazos en este fragmento de lápiz mientras \_ (más trazos ... ) { AddStroke(hrc, NULL, 800, pPacket, pXForm); // una llamada por trazo } EndInkInput(hrc); Esto obtiene el proceso reconocido por la entrada de lápiz (hrc); Si se trata de una aplicación sencilla, llama a esto para obtener una respuesta simple GetBestResultString(hrc, length, buffer); Si se trata de una aplicación compleja, lo llama para obtener una respuesta completa GetLatticePtr(hrc, &pLattice); Destruir el contexto DestroyContext(hrc); } // Llamado justo antes de que la aplicación cierre DestroyRecognizer(hrec);'
ms.assetid: 484ba140-788f-4b71-9cc7-9baa919d9936
title: Secuencia de llamada típica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94506d320d2ac0dca31fcc44714d0fd9ed089a2dda479020d860b0fbe5bfae5a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119708225"
---
# <a name="typical-calling-sequence"></a>Secuencia de llamada típica

Las API de la plataforma de Tablet PC llaman a los métodos que debe implementar para crear un reconocedor de entrada de lápiz y no directamente a una aplicación habilitada para lápiz.

Los pasos siguientes representan una secuencia de llamada típica para la implementación de estos métodos:

1.  Se carga el archivo DLL.
2.  Se [crea un identificador HRECOGNIZER.](hrecognizer-handle.md)
3.  Se [crea un identificador HRECOCONTEXT.](hrecocontext-handle.md)
4.  Las opciones y los modos del reconocedor se establecen para este contexto.
5.  Los trazos se agregan a los datos de entrada de lápiz.
6.  La entrada ha finalizado.
7.  Se reconoce la entrada de lápiz.
8.  Se devuelven los resultados del reconocimiento.
9.  Se [destruye el identificador HRECOCONTEXT.](hrecocontext-handle.md)
10. Se destruye el identificador [HRECOGNIZER.](hrecognizer-handle.md)

La secuencia de llamada también se muestra en el siguiente esquema de código:


```C++
CreateRecognizer(CLSID, &hrec);
while (more pieces of ink to recognize ... )
{
  // Create a context, once per piece of ink to be recognized
  hrc = CreateContext(hrec, &hrc);

  // Functions to set up options and modes for this context
  SetGuide(hrc, pGuide, 0);
  SetFactoid(hrc, 5, PHONE); // only if in application with forms
  SetFlags(hrc, RECOFLAG_WORDMODE); // rare, only if wanting word mode, no out-of-dictionary, or single segmentation
  SetWordList(hrc, hwl);

  // Adding all the strokes in this piece of ink
  while (more strokes ... )
  {
    AddStroke(hrc, NULL, 800, pPacket, pXForm);  // one call per stroke
  }
  EndInkInput(hrc);

  // This gets the ink recognized
  Process(hrc);

  // If this is a simple application, it calls this for a simple answer
  GetBestResultString(hrc, length, buffer);

  // If this is a complex application, it calls this for a complete answer
  GetLatticePtr(hrc, &pLattice);

  // Destroy the context
  DestroyContext(hrc);
}
// Called just before the application shuts down
DestroyRecognizer(hrec);
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[API de reconocedor](recognizer-apis.md)
</dt> <dt>

[Arquitectura de API de reconocimiento](recognition-api-architecture.md)
</dt> </dl>

 

 



