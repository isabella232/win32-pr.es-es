---
description: En este tema se describen las distintas maneras en las que puede crear instancias de un control InkEdit.
ms.assetid: 3ab0f10e-1a0d-4d0b-b5b2-69dc96570b33
title: Crear instancias de InkEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bde7e94566b076a4d9d6f6928fc08199ee71fa19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497650"
---
# <a name="instantiating-inkedit"></a>Crear instancias de InkEdit

En este tema se describen las distintas maneras en las que puede crear instancias de un control [InkEdit](inkedit-control.md) .

## <a name="visual-basic-net-and-c"></a>Visual Basic .NET y C\#

Si está trabajando con Microsoft Visual Basic .NET o C \# , arrastre el control [InkEdit](./inkedit-control.md) desde el cuadro de herramientas de Visual Studio hasta el formulario o la página donde desee que aparezca el control.

## <a name="win32c"></a>Win32/C++

El control [InkEdit](inkedit-control-reference.md) es una superclase del control Rich Edit 4,5 Win32 OLE incrustable.

Las aplicaciones Win32 crean una instancia del control [InkEdit](inkedit-control-reference.md) llamando a [CreateWindow ()](/windows/win32/api/winuser/nf-winuser-createwindowa) y pasando InkEdit como clase de ventana. INKEDIT se define en el. h. Una vez creado el control, puede "hablar" con el control con los mensajes. Los mensajes Rich Edit (EM \_ \* ) se pasan desde InkEdit a Rich Edit sin modificar; toda la funcionalidad de edición enriquecida existente está disponible.

Para crear un control [InkEdit](inkedit-control-reference.md) , llame a la función [CreateWindow ()](/windows/win32/api/winuser/nf-winuser-createwindowa) , especificando la clase de ventana InkEdit. Use [LoadLibrary ()](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) para registrar InkEd.dll. Especifique la \_ constante definida por la clase INKEDIT para el parámetro de clase de ventana y use los estilos de ventana que se especifican en los ejemplos siguientes.

### <a name="instantiating-a-multiline-inkedit-control"></a>Crear una instancia de un control InkEdit de varias líneas


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



### <a name="instantiating-a-single-line-inkedit-control"></a>Crear una instancia de un control Single-Line InkEdit


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
> A diferencia de RichEdit, debe asegurarse de llamar a [CoInitialize ()](/windows/win32/api/objbase/nf-objbase-coinitialize) antes de crear el control [InkEdit](inkedit-control-reference.md) . Llame a [CoUninitialize ()](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) cuando se cierre la aplicación. Después de llamar a CoUninitialize (), debe llamar a [FreeLibrary (s \_ hlib)](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) para reducir el recuento de referencias en el archivo de InkEdit.dll.

 

Si usa el estilo de ventana [ \_ NOIME es](../controls/rich-edit-control-styles.md) , la compatibilidad con la corrección integrada no está disponible. Si no se especifica una ventana primaria, el control se crea como una ventana de nivel superior y \_ se agrega el estilo WS SYSMENU; de esta forma, también se deshabilita la compatibilidad con la corrección integrada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Agregar controles de entrada manuscrita a un proyecto](adding-ink-controls-to-a-project.md)
</dt> </dl>

 

 
