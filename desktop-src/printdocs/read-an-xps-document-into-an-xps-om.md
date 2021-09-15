---
description: Describe cómo leer un documento XPS existente de un archivo en un OM XPS.
ms.assetid: 92a8d19f-1c9e-4e02-a3d4-f2869ec871df
title: Leer un documento XPS en un OM XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5c3b703de24be58db875618b575cebf9c1c0b27
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127248384"
---
# <a name="read-an-xps-document-into-an-xps-om"></a>Leer un documento XPS en un OM XPS

Describe cómo leer un documento XPS existente de un archivo en un OM XPS.

Para crear una OM XPS a partir de un documento XPS, llame al método [**IXpsOMObjectFactory::CreatePackageFromFile.**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromfile)

Antes de usar estos ejemplos de código en el programa, lea la declinación de responsabilidades en [Tareas comunes de programación de documentos XPS](common-xps-document-tasks.md).

## <a name="code-example"></a>Ejemplo de código

En el ejemplo de código siguiente se da por supuesto que la inicialización descrita en [Inicialización de una OM XPS](xps-object-model-initialization.md) se ha hecho correctamente.


```C++
    IXpsOMPackage *package = NULL;

    hr = xpsFactory->CreatePackageFromFile(
        xpsDocumentFilename,
        FALSE,
        &package);

    // package now contains a pointer to the IXpsOMPackage
    // object that has been populated with the contents
    // of the XPS document in xpsDocumentFilename.

    // When finished with the package, release the object.
    if (NULL != package) package->Release();
```



Para crear una OM XPS a partir de un documento XPS que se almacena como una secuencia, llame a [**IXpsOMObjectFactory::CreatePackageFromStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromstream).

## <a name="remarks"></a>Observaciones

Si escribe un XPS OM inmediatamente después de haber leído un paquete XPS en él, es posible que parte del contenido original se pierda o cambie.

Algunos de los cambios que pueden producirse en este caso se enumeran en la tabla siguiente:

| Característica de documento                      | Acción                                                             |
|---------------------------------------|--------------------------------------------------------------------|
| Firmas digitales<br/>         | Se ha quitado del documento.<br/>                               |
| Elemento DiscardControl<br/>        | Se ha quitado del documento.<br/>                               |
| Elementos de documentos externos<br/>     | Se ha quitado del documento.<br/>                               |
| Marcado FixedPage<br/>           | Modificado a partir del original<br/>                              |
| Marcado del diccionario de recursos<br/> | Se ha modificado a partir del original, si se ha establecido la marca Optimización<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Pasos siguientes**
</dt> <dt>

[Navegación por XPS OM](navigate-the-xps-om.md)
</dt> <dt>

[Escribir texto en una om xps](write-text-to-an-xps-om.md)
</dt> <dt>

[Dibujar gráficos en un OM XPS](draw-graphics-in-an-xps-om.md)
</dt> <dt>

[Colocar imágenes en un OM xps](place-images-in-an-xps-om.md)
</dt> <dt>

**Se usa en esta sección**
</dt> <dt>

[**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

**Para obtener más información**
</dt> <dt>

[Inicialización de una om xps](xps-object-model-initialization.md)
</dt> <dt>

[API de empaquetado](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[Referencia de document API de XPS](xps-programming-reference.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

