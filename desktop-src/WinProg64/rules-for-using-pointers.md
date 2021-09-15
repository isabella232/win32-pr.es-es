---
title: Reglas para usar punteros
description: La porción del código para compilar para microsoft de 32 y 64 Windows es sencilla. Solo necesita seguir algunas reglas sencillas sobre la conversión de punteros y usar los nuevos tipos de datos en el código. Las reglas para la manipulación de punteros son las siguientes.
ms.assetid: 4c38bee2-fa1c-493f-a12d-e673df4d4895
keywords:
- reglas para usar punteros de 64 bits Windows programación
- Manipulación de punteros de 64 bits Windows programación
- conversión de punteros de 64 bits Windows programación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 318ff5beed6dc90bd49b6b293131e17db6f92f6b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476127"
---
# <a name="rules-for-using-pointers"></a>Reglas para usar punteros

La porción del código para compilar para microsoft de 32 y 64 Windows es sencilla. Solo necesita seguir algunas reglas sencillas sobre la conversión de punteros y usar los nuevos tipos de datos en el código. Las reglas para la manipulación de punteros son las siguientes.

1.  No convertir punteros a **int**, **long,** **ULONG** o **DWORD.**

    Si debe convertir un puntero para probar algunos bits, establecer o borrar bits, o manipular su contenido, use el tipo **\_ UINT PTR** **o INT \_ PTR.** Estos tipos son tipos enteros que se escalan al tamaño de un puntero para Windows de 32 y 64 bits (por ejemplo, **ULONG** para Windows de 32 bits e int64 para Windows \_ de 64 bits). Por ejemplo, suponga que está porteando el código siguiente:

    `ImageBase = (PVOID)((ULONG)ImageBase | 1);`

    Como parte del proceso de porte, cambiaría el código de la manera siguiente:

    `ImageBase = (PVOID)((ULONG_PTR)ImageBase | 1);`

    Use **UINT \_ PTR** e **INT \_ PTR** cuando corresponda (y si no está seguro de si son necesarios, no hay ningún daño al usarlos por si fuera necesario). No convierte los punteros a los tipos **ULONG,** **LONG,** **INT,** **UINT** o **DWORD.**

    Tenga en cuenta que **HANDLE** se define como **un valor void \* *_,*** por lo que convertir un valor _ HANDLE en un valor **ULONG** para probar, establecer o borrar los 2 bits de orden inferior es un error en los bits de 64 Windows.

2.  Use las **funciones PtrToLong** **o PtrToUlong** para truncar punteros.

    Si debe truncar un puntero a un valor de 32 bits, use la función **PtrToLong** o **PtrToUlong** (definida en Basetsd.h). Estas funciones deshabilitan la advertencia de truncamiento del puntero mientras dure la llamada.

    Use estas funciones con cuidado. Después de convertir una variable de puntero mediante una de estas funciones, no vuelva a usarla como puntero. Estas funciones truncan los 32 bits superiores de una dirección, que normalmente son necesarios para acceder a la memoria a la que hace referencia originalmente el puntero. El uso de estas funciones sin tener en cuenta cuidadosamente dará lugar a un código frágil.

3.  Tenga cuidado al usar valores POINTER \_ 32 en código que se pueden compilar como código de 64 bits. El compilador firmará el puntero cuando se asigne a un puntero nativo en código de 64 bits, no extenderá el puntero a cero.
4.  Tenga cuidado al usar valores POINTER \_ 64 en código que se pueden compilar como código de 32 bits. El compilador firmará la extensión del puntero en código de 32 bits, no en el puntero de extensión cero.
5.  Tenga cuidado con el uso de parámetros OUT.

    Por ejemplo, supongamos que tiene una función definida de la siguiente manera:

    `void func( OUT PULONG *PointerToUlong );`

    No llame a esta función como se muestra a continuación.

    ``` syntax
    ULONG ul;
    PULONG lp;
    func((PULONG *)&ul);
    lp = (PULONG)ul;
    ```

    En su lugar, use la siguiente llamada.

    ``` syntax
    PULONG lp;
    func(&lp);
    ```

    La &de tipo ul a **PULONG \*** evita un error del compilador, pero la función escribirá un valor de puntero de 64 bits en la memoria en &ul. Este código funciona en Windows de 32 bits, pero provocará daños en los datos en el Windows de 64 bits y será sutil y difícil de encontrar. La línea de fondo: No jugar a trucos con el código C: es mejor sencillo y sencillo.

6.  Tenga cuidado con las interfaces polimórficas.

    No cree funciones que acepten **parámetros DWORD** para datos polimórficos. Si los datos pueden ser un puntero o un valor entero, use el tipo \_ UINT PTR **o PVOID.**

    Por ejemplo, no cree una función que acepte una matriz de parámetros de excepción con el tipo **de valores DWORD.** La matriz debe ser una matriz de **valores \_ DWORD PTR.** Por lo tanto, los elementos de la matriz pueden contener direcciones o valores enteros de 32 bits. (La regla general es que, si el tipo original es **DWORD** y debe tener un ancho de puntero, conviénelo en un **valor \_ DWORD PTR.** Por eso hay tipos de precisión de puntero correspondientes). Si tiene código que usa **DWORD,** **ULONG** u otros tipos de 32 bits de forma polimórfica (es decir, realmente quiere que el miembro de parámetro o estructura mantenga una dirección), use **UINT \_ PTR** en lugar del tipo actual.

7.  Use las nuevas funciones de clase de ventana.

    Si tiene datos privados de ventana o clase que contienen punteros, el código deberá usar las siguientes funciones nuevas:

    -   [**GetClassLongPtr**](/windows/win32/api/winuser/nf-winuser-getclasslongptra)
    -   [**GetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-getwindowlongptra)
    -   [**SetClassLongPtr**](/windows/win32/api/winuser/nf-winuser-setclasslongptra)
    -   [**SetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra)

    Estas funciones se pueden usar en las funciones de 32 y 64 Windows, pero son necesarias en el Windows de 64 bits. Prepárese para la transición mediante estas funciones ahora.

    Además, debe tener acceso a punteros o identificadores en datos privados de clase mediante las nuevas funciones de 64 bits Windows. Para ayudar a encontrar estos casos, los siguientes índices no se definen en Winuser.h durante una compilación de 64 bits:

    -   \_WNDPROC de GWL
    -   GWL \_ HINSTANCE
    -   GWL \_ HWDPARENT
    -   GWL \_ USERDATA

    En su lugar, Winuser.h define los siguientes índices nuevos:

    -   GWLP \_ WNDPROC
    -   GWLP \_ HINSTANCE
    -   GWLP \_ HWNDPARENT
    -   GWLP \_ USERDATA
    -   Id. de \_ GWLP

    Por ejemplo, el código siguiente no se compila:

    `SetWindowLong(hWnd, GWL_WNDPROC, (LONG)MyWndProc);`

    Debe cambiarse como se muestra a continuación:

    `SetWindowLongPtr(hWnd, GWLP_WNDPROC, (LONG_PTR)MyWndProc);`

    Al establecer el **miembro cbWndExtra** de la estructura [**WNDCLASS,**](/windows/win32/api/winuser/ns-winuser-wndclassa) asegúrese de reservar suficiente espacio para los punteros. Por ejemplo, si está reservando actualmente bytes sizeof(DWORD) para un valor de puntero, reserve sizeof(DWORD \_ PTR) bytes.

8.  Acceda a todos los datos de ventana y clase mediante **FIELD \_ OFFSET**.

    Es habitual acceder a los datos de ventana mediante desplazamientos codificados de forma hard-code. Esta técnica no es portátil a 64 bits Windows. Para que el código sea portátil, acceda a los datos de la ventana y la clase mediante la macro **FIELD \_ OFFSET.** No suponga que el segundo puntero tiene un desplazamiento de 4.

9.  Los **tipos LPARAM,** **WPARAM** y **LRESULT** cambian de tamaño con la plataforma.

    Al compilar código de 64 bits, estos tipos se expanden a 64 bits, ya que normalmente contienen punteros o tipos enteros. No mezcle estos valores **con valores DWORD,** **ULONG,** **UINT,** **INT,** **int** o **long.** Examine cómo se usan estos tipos y asegúrese de que no trunca accidentalmente los valores.

 

 