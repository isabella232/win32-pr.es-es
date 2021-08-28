---
title: Nuevos tipos de datos
description: Se introdujeron tres clases de tipos de datos para tipos de datos de 64 bits Windows de precisión fija, tipos de precisión de puntero y tipos de precisión de puntero específicos.
ms.assetid: 016977d4-e7bf-463e-9755-7ef13f16e9e5
keywords:
- Guía de programación de 64 Windows de programación de 64 Windows programación, tipos de datos
- tipos de datos de 64 bits Windows programación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddc3cc6615de7c93c805eac868536b53084a694fb79d4e63d908716eb026eb71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119504845"
---
# <a name="the-new-data-types"></a>Nuevos tipos de datos

Se introdujeron tres clases de tipos de datos para tipos de datos de 64 Windows: tipos de datos de precisión fija, tipos de precisión de puntero y tipos de precisión de puntero específicos. Estos tipos se agregaron al entorno de desarrollo para permitir a los desarrolladores prepararse para las aplicaciones de 64 Windows. Estos tipos se derivan del entero básico del lenguaje C y de los tipos long. Por lo tanto, puede usar estos tipos de datos en código que compile y pruebe en un Windows de 32 bits y, a continuación, vuelva a compilar con el compilador de 64 bits cuando el destino sea Windows de 64 bits.

Incluso en el caso de las aplicaciones que tienen como destino solo Windows 32 bits, la adopción de estos nuevos tipos de datos hace que el código sea más sólido. Para usar estos tipos de datos, debe examinar el código en busca de definiciones de datos, polimorfismo y uso de puntero potencialmente no seguros. Por ejemplo, cuando una variable es de tipo **ULONG \_ PTR**, está claro que se usará para convertir punteros para operaciones aritméticas o polimorfismo. No es posible indicar este uso directamente mediante los tipos de datos anteriores. (Puede hacerlo indirectamente mediante la nomenclatura de tipos derivados o la notación húngaro, pero ambas técnicas son propensas a errores).

Todos estos tipos de datos se declaran en BaseTsd.h. Para obtener más información, incluidas las definiciones de estos tipos de datos, [vea Windows Data Types](/windows/desktop/WinProg/windows-data-types).

## <a name="fixed-precision"></a>Precisión fija

Los tipos de datos de precisión fija tienen la misma longitud en los tipos de datos de 32 y 64 Windows. Para ayudarle a recordar esto, su precisión forma parte del nombre del tipo de datos. A continuación se enumeran los tipos de datos de precisión fija.



| Término                                                                       | Descripción                        |
|----------------------------------------------------------------------------|------------------------------------|
| <span id="DWORD32"></span><span id="dword32"></span>**DWORD32**<br/> | Entero de 32 bits sin signo<br/> |
| <span id="DWORD64"></span><span id="dword64"></span>**DWORD64**<br/> | Entero de 64 bits sin signo<br/> |
| <span id="INT32"></span><span id="int32"></span>**INT32**<br/>       | Entero de 32 bits con signo<br/>   |
| <span id="INT64"></span><span id="int64"></span>**INT64**<br/>       | Entero de 64 bits con signo<br/>   |
| <span id="LONG32"></span><span id="long32"></span>**LONG32**<br/>    | Entero de 32 bits con signo<br/>   |
| <span id="LONG64"></span><span id="long64"></span>**LONG64**<br/>    | Entero de 64 bits con signo<br/>   |
| <span id="UINT32"></span><span id="uint32"></span>**UINT32**<br/>    | **INT32** sin signo<br/>      |
| <span id="UINT64"></span><span id="uint64"></span>**UINT64**<br/>    | **INT64** sin signo<br/>      |
| <span id="ULONG32"></span><span id="ulong32"></span>**ULONG32**<br/> | **LONG32 sin signo**<br/>     |
| <span id="ULONG64"></span><span id="ulong64"></span>**ULONG64**<br/> | **LONG64** sin signo<br/>     |



 

## <a name="pointer-precision"></a>Precisión del puntero

A medida que cambia la precisión del puntero (es decir, cuando se convierte en 32 bits en Windows de 32 bits y 64 bits con Windows de 64 bits), los tipos de datos de precisión de puntero reflejan la precisión en consecuencia. Por lo tanto, es seguro convertir un puntero a uno de estos tipos al realizar operaciones aritméticas de puntero; si la precisión del puntero es de 64 bits, el tipo es de 64 bits. Los tipos de recuento también reflejan el tamaño máximo al que puede hacer referencia un puntero. A continuación se enumeran los tipos de precisión de puntero y recuento.



| Término                                                                              | Descripción                                                                                                                      |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span id="DWORD_PTR"></span><span id="dword_ptr"></span>**DWORD \_ PTR**<br/> | Tipo largo sin signo para la precisión del puntero.<br/>                                                                             |
| <span id="HALF_PTR"></span><span id="half_ptr"></span>**HALF \_ PTR**<br/>    | La mitad del tamaño de un puntero. Use dentro de una estructura que contiene un puntero y dos campos pequeños.<br/>                      |
| <span id="INT_PTR"></span><span id="int_ptr"></span>**INT \_ PTR**<br/>       | Tipo entero con signo para la precisión del puntero.<br/>                                                                            |
| <span id="LONG_PTR"></span><span id="long_ptr"></span>**LONG \_ PTR**<br/>    | Tipo long con firma para la precisión del puntero.<br/>                                                                               |
| <span id="SIZE_T"></span><span id="size_t"></span>**SIZE \_ T**<br/>          | Número máximo de bytes a los que puede hacer referencia un puntero. Se usa para un recuento que debe abarcar el intervalo completo de un puntero.<br/> |
| <span id="SSIZE_T"></span><span id="ssize_t"></span>**SSIZE \_ T**<br/>       | Tamaño **con \_ firma T**.<br/>                                                                                                   |
| <span id="UHALF_PTR"></span><span id="uhalf_ptr"></span>**UHALF \_ PTR**<br/> | HALF PTR sin **\_ signo.**<br/>                                                                                               |
| <span id="UINT_PTR"></span><span id="uint_ptr"></span>**UINT \_ PTR**<br/>    | INT **\_ PTR sin signo.**<br/>                                                                                                |
| <span id="ULONG_PTR"></span><span id="ulong_ptr"></span>**ULONG \_ PTR**<br/> | LONG **\_ PTR sin signo.**<br/>                                                                                               |



 

## <a name="specific-pointer-precision-types"></a>Tipos de Pointer-Precision específicos

Los siguientes nuevos tipos de puntero tamaño explícitamente el puntero. Tenga cuidado al usar punteros en código de 64 bits: si declara el puntero mediante un tipo de 32 bits, el sistema operativo crea el puntero truncando un puntero de 64 bits. (Todos los punteros son de 64 bits en Windows de 64 bits).



| Término                                                                                 | Descripción                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="POINTER_32"></span><span id="pointer_32"></span>**PUNTERO \_ 32**<br/> | Puntero de 32 bits. En los Windows de 32 bits, se trata de un puntero nativo. En el caso de Windows de 64 bits, se trata de un puntero truncado de 64 bits.<br/>                                                                                       |
| <span id="POINTER_64"></span><span id="pointer_64"></span>**PUNTERO \_ 64**<br/> | Puntero de 64 bits. En un Windows de 64 bits, se trata de un puntero nativo. En el caso de Windows de 32 bits, se trata de un puntero de 32 bits extendido por signo. <br/> Tenga en cuenta que no es seguro asumir el estado del bit de puntero alto.<br/> |



 

 

