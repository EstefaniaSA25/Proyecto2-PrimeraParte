# Proyecto2-PrimeraParte
Primera parte del segundo proyecto de Python Avanzado

# FotoApp – Proyecto 2

### Tecnicatura Universitaria en Tecnologías de Programación  
**Materia:** Programación Python Avanzada  
**Integrantes:** Amezaga Estefanía, Figueroa Cynthia, Pizarro Sol.  

## Descripción
FotoApp es una aplicación para procesar y editar imágenes en Python.  
Permite redimensionar, mejorar contraste, aplicar filtros, crear bocetos y manejar todas las funciones desde un menú interactivo.

## Funcionalidades principales
1. Redimensionar imágenes según red social (Instagram, Facebook, Twitter, YouTube)
2. Ajustar contraste mediante ecualización de histograma
3. Aplicar los 9 filtros de Pillow
4. Crear bocetos tipo dibujo (bordes o lápiz)
5. Menú interactivo con manejo de errores

## Diagrama de flujo del menú principal
```
                   ┌────────────────────┐
                   │   Inicio FotoApp   │
                   └─────────┬──────────┘
                             │
                             ▼
                ┌──────────────────────────────┐
                │ Pedir URL o ruta de imagen   │
                └─────────┬────────────────────┘
                          │
                          ▼
                ┌──────────────────────────────┐
                │   Mostrar menú principal     │
                └─────────┬────────────────────┘
                          │
          ┌───────────────┼───────────────┬───────────────┬───────────────┬───────────────┐
          ▼               ▼               ▼               ▼               ▼               ▼
   ┌────────────┐  ┌───────────────┐  ┌────────────────┐  ┌───────────────┐   ┌────────────────┐   ┌───────────────┐
   │  Opción 1  │  │   Opción 2    │  │    Opción 3    │  │    Opción 4   │   │    Opción 5    │   │   Opción 6    │
   │Redimension │  │Ajustar cont.  │  │Aplicar filtro  │  │  Crear boceto │   │ Cambiar imagen │   │     Salir     │
   └─────┬──────┘  └──────┬────────┘  └──────┬─────────┘  └──────┬────────┘   └──────┬─────────┘   └──────┬────────┘
         │                │                  │                   │                   │                    │
         ▼                ▼                  ▼                   ▼                   ▼                    ▼
 Ejecutar función   Ejecutar función   Ejecutar función   Ejecutar función     Pedir nueva ruta       Finalizar app
 redimensionar()    ajustar_contraste() aplicar_filtro()  crear_boceto()       y actualizar var.         
         │                 │                 │                  │                 │                  
         └─────────────────┴─────────────────┴──────────────────┴─────────────────┴
                                             │
                                             ▼
                                   ┌────────────────────┐
                                   │   Retornar al menú │
                                   └────────────────────┘

```

## Archivos del proyecto
- `fotoapp.py` → módulo con todas las funciones  
- `fotoapp_testdev.ipynb` → notebook de pruebas y resultados  
- Carpeta `/imagenes` → imágenes de prueba y generadas  

### Librerías utilizadas
`pillow`, `matplotlib`, `opencv-python`, `numpy`, `requests`

## Ejecución
1. Importar el módulo:
   ```python
   from fotoapp import menu_principal
   menu_principal()
