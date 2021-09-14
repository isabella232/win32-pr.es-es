---
description: En este tema se describen las distintas formas de crear instancias de un control InkEdit.
ms.assetid: 3ab0f10e-1a0d-4d0b-b5b2-69dc96570b33
title: Creación de instancias de InkEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bde7e94566b076a4d9d6f6928fc08199ee71fa19
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359639"
---
# <a name="instantiating-inkedit"></a>Creación de instancias de InkEdit

En este tema se describen las distintas formas de crear instancias de un control [InkEdit.](inkedit-control.md)

## <a name="visual-basic-net-and-c"></a>Visual Basic .NET y C\#

Si está trabajando con Microsoft Visual Basic .NET o C, arrastre el control InkEdit desde el cuadro de herramientas de Visual Studio hasta el formulario o la página donde desea que aparezca \# el control. [](./inkedit-control.md)

## <a name="win32c"></a>Win32/C++

El control [InkEdit](inkedit-control-reference.md) es una superclase del control insertable RICH Edit 4.5 Win32 OLE.

Las aplicaciones Win32 crean instancias del control [InkEdit](inkedit-control-reference.md) llamando a [CreateWindow()](/windows/win32/api/winuser/nf-winuser-createwindowa) y pasando INKEDIT como clase de ventana. INKEDIT se define en InkEd.h. Una vez creado el control, puede "hablar" con el control con mensajes. Los mensajes rich edit (EM) se pasan de InkEdit a Rich Edit sin modificar; toda la funcionalidad rich edit existente \_ \* está disponible.

Para crear un control [InkEdit,](inkedit-control-reference.md) llame a [la función CreateWindow()](/windows/win32/api/winuser/nf-winuser-createwindowa) y especifique la clase de ventana InkEdit. Use [LoadLibrary() para](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) registrar InkEd.dll. Especifique la constante INKEDIT CLASS definida para el parámetro de clase window y use los estilos de ventana como se \_ especifica en los ejemplos siguientes.

### <a name="instantiating-a-multiline-inkedit-control"></a>Creación de instancias de un control InkEdit multilínea


```C++
//...
HMODULE s_hlib;    
s_hlib= LoadLibrary("InkEd.dll");
//...
m_hwndInkEdit = CreateWindowW(INKEDIT_CLASS, NULL,
WS_CHILD|WS_VISIBLE|WS_BORDER|ES_MULTILINE,
rt.left, rt.top, rt.right, rt.bottom,
m_hWnd, NULL, hInst, NULL);
```



### <a name="instantiating-a-single-line-inkedit-control"></a>Creación de instancias de un Single-Line Control InkEdit


```C++
//...
HMODULE s_hlib;    
s_hlib= LoadLibrary("InkEd.dll");
//...
m_hwndInkEdit = CreateWindowW(INKEDIT_CLASS, NULL,
WS_CHILD|WS_VISIBLE|WS_BORDER,
rt.left, rt.top, rt.right, rt.bottom,
m_hWnd, NULL, hInst, NULL);
```



> [!Note]  
> A diferencia de RichEdit, debe asegurarse de llamar a [CoInitialize()](/windows/win32/api/objbase/nf-objbase-coinitialize) antes de crear el control [InkEdit.](inkedit-control-reference.md) Llame [a CoUninitialize()](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) cuando se cierre la aplicación. Después de llamar a CoUninitialize(), debe llamar a [FreeLibrary(s \_ hlib)](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) para disminuir el recuento de referencias en el InkEdit.dll archivo.

 

Si usa el estilo [de ventana \_ ES NOIME,](../controls/rich-edit-control-styles.md) la compatibilidad con la corrección integrada no está disponible. Si no especifica una ventana primaria, el control se crea como una ventana de nivel superior y se agrega el estilo SYSMENU de WS; esto también deshabilita la compatibilidad con la corrección \_ integrada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Agregar controles ink a un Project](adding-ink-controls-to-a-project.md)
</dt> </dl>

 

 
